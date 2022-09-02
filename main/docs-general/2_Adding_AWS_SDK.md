Priviously, there we several ways to add the aws-iot-device-adk-embedded-c library.  The advice on this seems to be changing.

Curently we add this SDK in the following way.   NOTE: This method has not been fully tested/verified YET Aug19-22


1) build a sample project that is empty.

2) navigate in Git Bash to the root directory

3) In Git Bash run:   git clone https://github.com/aws/aws-iot-device-sdk-embedded-c.git --recurse-submodules


Here is the guide:

https://docs.aws.amazon.com/iot/latest/developerguide/iot-embedded-c-sdk.html

DO NOT INSTALL OpenSSL as described in this document.   You should have it already in 
place.  Type  "openssl version" on a Git Bash command prompt and see if you receive:

OpenSSL 1.1.1q  5 Jul 2022

This OpenSSL tool is required based on the assumption that you are going to use Code Signing for AWS IoT to sign your firmware images.

I suspect this tool was installed with the ESP-IDF and tools operations when calling "Configure ESP-IDF Extension" in VS Code.