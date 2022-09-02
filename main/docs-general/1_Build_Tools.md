Build Tools Required for AWS IOT Embedded Projects -- Windows 10

(Listed in the order in which I installed them)

1) VS Code (accepted all defaults)
   Added Esprssif IDF Plug-in
   Added C/C++ Extension Pack

From Command Palette: ESP-IDF:Configure ESP-IDF Extension      accept defaults.
NOTE: Espressif IDF Plug-in will install Cross Compilers, Python, ESP-IDF, CMake, Ninja build tools, and the current ESP-IDF.  

As of August 15th-22, the configuration action will install:
   IDF v4.4.1
   Git v2.23.1
   Python v3.8.7

2) Github Tools (https://git-scm.com/download/win)

Accept all defaults and all tools.  I personally only use Git Bash.


3) AWS CLI Version 2

https://awscli.amazonaws.com/AWSCLIV2.msi

With Git Bash Run AWS Configure and enter your Access Key ID, Secret Access Key, Default region name, and Default output format (this assumes you already have an active AWS account)
