# CMD Managing User Accounts Lab
We can manage user accounts on our local machine using the CMD's NET USER command.

## Displaying User Accounts
We can display all of the user accounts on our local computer by using the the ```NET USER``` with no arguments.

![View Local Accounts](.\assets\view-local-accounts.png)

## Displaying Information About a Specific User Account
We can view information about a specific user account by using ```NET USER <USERNAME>``` with a specific user account name. For example, ```NET USER Admin```.

![Display Local Account Information](.\assets\display-local-account-information.png)

We will go over a few fields:<br/>
<b>Account active</b> - Indicates whether an account is active or not.
<b>Account expires</b> - Indicates when the account is going to expire (never in this instance). However, this may be used with a temporary employee or guest. </br>
<b>Last logon</b> - When the user last logged on. <br/>
<b>Logon hours allowed</b> - What times the user is able to logon. This can be used for setting business hours or screen time for employees or children.

## Adding a User Account
We can add a user account by using ```NET USER <USERNAME> /ADD``` as an administrator. If we want to add a password to the account we would user ```NET USER <USERNAME> <PASSWORD> /ADD /PASSWORDREQ:YES``` (note: passwords are case sensitive). Lastly, we can add a full name to the account by adding the FULLNAME switch. ```NET USER <USERNAME> <PASSWORD> /ADD /PASSWORDREQ:YES /FULLNAME:<NAME>```.

![Create New User](.\assets\create-new-user.png)

We can see the details below:

![Show New User](.\assets\show-new-user.png)

## Disabling and Deleting a User Account
We can disable and delete a user account as well. We may need to do this as this can pose a security risk if a bad actor guesses the correct password for a user, especially a privileged user.

To disable a user we run ```NET USER <USERNAME> /ACTIVE:NO``` as an administrator.

![Disable a User Account](.\assets\disable-user-account.png)

To delete a user account we run ```NET USER <USERNAME> /DELETE``` as an administrator.

![Delete User](.\assets\delete-user.png)