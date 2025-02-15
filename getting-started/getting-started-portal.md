# Getting started with the Yoda Portal

## Logging in
Go to [https://portal.yoda.vu.nl/](https://portal.yoda.vu.nl/)

Log in using the "Sign in" button. You will be prompted for your email address. If you are an employee or student 
at Vrije Universiteit, your user name is your primary email address (in lowercase). 

![](screenshots/portal_login.png)

Click Next. VU users will be forwarded to the familiar VU login page. External users have usually received their user name
via email, along with a link to set their password.

VU users have to login with Multi Factor Authentication (MFA). Note that instead of the TiQR app you should now use the 
more user-friendly Azure MFA. Switch by following [this instruction manual](https://vunl.sharepoint.com/:f:/r/sites/Collaboration-Services/Identity%20and%20security/Tiqr%20-%20MFA%20Manuals?csf=1&web=1&e=KhnHHc) 
on the VU SharePoint.

## Overview of the Yoda Portal
### Group Manager
Yoda allows you to store your valuable research data in a secure way.  The data is kept in data compartments,
which can only be accessed by members.

The Group Manager can be used to view a list of data compartments and their members. People with a "group manager" role
can add members to a data compartment, remove them, and change their roles.

See: [Managing groups, users and access rights](user-management.html)

### Your data in the Yoda Portal
Each group in Yoda has two main folders:

#### Research
The main folder ("research-...") contains current research data that researchers
collaborate on. Data is kept in subfolders. The subfolders can be organized according
to the needs of the researcher.

You can also drag-and-drop files to your research folder.

![img.png](screenshots/research-drag-drop.png)

#### Archiving
After completion of a study, the data in that subfolder can be deposited so that it is
kept for 10 years or longer. Use the "Submit" button to deposit the subfolder. This will
copy the contents of the subfolder to the Vault folder as a new data package.
Before doing so, the subfolder must be described with metadata, which can be entered by
clicking on the Metadata button. 

For more information on metadata in Yoda see: [Metadata in Yoda](metadata-add.md).

#### Vault
The folder named "vault-..." contains deposited data packages.
Once deposited, data cannot be removed. Therefore the vault can be used to account for data
in a research project to comply with FAIR principles.

#### Publishing
Researchers can opt to (but do not have to) publish any of the vault deposited data packages
to make the metadata description of a data package known to the research community at large.
Yoda adds a DOI persistent identifier to published data so that the data package can be cited
and found in catalogs such as Datacite, Narcis, B2Find etcetera.
If (and only if) the data has been classified as "open" then the content itself can be downloaded
by anyone from the internet. Otherwise, only the metadata description can be viewed.
