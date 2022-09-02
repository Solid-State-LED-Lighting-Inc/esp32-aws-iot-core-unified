AWS Setup

Assuming you already have a working AWS account...

1) Create a working Master_User (has administrative privileges).  

This is your administration account which is NOT the root user.  This is the user you will register inside your development computer for AWS CLI work.

a)Sign in with your root email address and password.  

b)Enter the AWS IAM subsystem.  Move to Users and create a new user with a chosen name.  This will be your working user account.

I have chosen Master_User   

c) Select "Access key - Programmatic access".  Next select "Add Permissions".  Click on "Attach existing policies directly" search for "AdministratorAccess" and check that box.  Click next.  Click Review (skipping tags) Click "Create User"   

Copy and store your Access key ID and Secret access key.

You now have a Master_User who can administer all your work.   Use these keys in Git Bash to configure AWS.

AWS Configure
<enter Access Key ID>
<enter Secret Access key>
<enter Default region name>
<enter Default output format>

Test your Master_User with this command in Git bash:  aws iot list-things



The next information will cover the creation of the following:

    1) Policies
    2) Certificatates
    3) Roles
    4) Provision Template
    5) Thing groups
    6) Thing types




