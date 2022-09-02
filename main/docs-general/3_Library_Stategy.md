The original work was based on aws-iot-device-sdk-embedded-C version 202103.00 (March 2021).   At that time, the library was not in very organized condition and the fleet provisioning example was completely inconsistant with the remainder of library.

The new version 202108.00 (August 2021), seems to be a leap foward and the libraries are nicely organized and consistant.

STILL, the bulk of the work is non-integrated.  The libraries are making calls which are to some extent are duplicated in other libraries.

The design here is to integrate the libraries into one cohesive task which can handles incoming and outgoing messages based on state.

Currently we integrate these AWS libraries into one:
    device-shadow-for-aws-iot-embedded-sdk
    fleet-provisioning-for-aws-iot-embedded-sdk
    jobs-for-aws-iot-embedded-sdk
    ota-for-aws-iot-embedded-sdk

We do NOT currently include these libraries:
    device-defender-for-aws-iot-embedded-sdk
    sigv4-for-aws-iot-embedded-sdk

Other libraries that will be referenced in the project:
    mbedtls
    tinycbor  (this may be in use for OTA -- TBD)
    backoffAlgorithm
    coreHTTP
    coreJSON
    coreMQTT
    corePKCS11
    cJSON      (Included as a component.  This library is used for json parsing and will be phased out)


NOTE about cJSON

http://www.json.org/

I found the entire tool in a platformIO/framework-espidf/components library.  I created a components directory in the root project space.  I copied the component over to the components directory of the project.  I included "cJSON.h" in my project and it was ready to go.

NOTE: There are two json parsers in action right now.  One will be removed.


