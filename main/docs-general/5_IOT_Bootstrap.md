WARNING: There can be a very significant confusion between IAM Roles/Policies and IOT Core Certificates/Policies.   The docs talk about the relationshp between the IOT Provisional Template and the IAM Role for Provisioning.

Each physical device as a "Non-Thing" must connect with what is considered a general certificate.   That certificate must be embedded in the program FLASH.


THREE CERTIFICATES:

My approach is to embedd 3 sets of general certificates in the program code.

Each set is: a Certificate PEM (privacy enhanced mail), a Private Key, and a Public Key.

The device will rotate through each set of credentials looking for one that will function.  With this approach, you may disable one or two of the certificates if you have suspecious activity on them.

This provides a solid way of always having a working general certificate available for an unprovisioned "Thing".


If you somehow destroy a Thing's certificate, it will automatically fall-back and reprovision again.   

NOTE: This could be one sure way to rotate a certificate, but AWS recommends that the Jobs feature be used for rotating certificates.


My previous work with AWS required that any connected device be authenticated through data in the Shadow.   Without a valid response from software in the Shadow a physical device was non-functional.

In the case where a device could function independantly of the Shadow, then an authentication list of MAC addresses would be a more certain way to avoid provisioning rogue devices which may be unauthorized to operate with this software but yet hold a general certificate.  AWS recommends this latter approach.


General Approach for device provisioning will be as follows:

1) A Device logs in with a working general certificate.
2) The Device already has the authorized IOT endpoint written in FLASH and uses that enpoint to connect.
3) A Device transmits its MAC address (the 6 digits which are unique)
4) A lamdba function will examine the MAC address and permit/reject the device.
5) If accepted, the system will impliment the Provisioning Template, create the Thing, Thing Name, and assign Certificates and Policies.
6) The system will return the newly created certificates back to the device.
7) The Device stores the certificate in NVS and logs out.
8) Device reconnects as a Thing.
9) The Device may access Jobs or the Shadow as needed.





















