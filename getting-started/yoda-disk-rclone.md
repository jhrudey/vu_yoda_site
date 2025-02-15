# Using rclone
[Rclone](https://rclone.org/) is a command-line program to manage files on cloud storage. 
It is a feature-rich alternative to cloud vendors' web storage interfaces. 
Over 40 cloud storage products support rclone including S3 object stores, business & consumer file storage services, 
as well as standard transfer protocols.

Rclone is available for Linux, Mac and Windows, see https://rclone.org/downloads/ 

You can use rclone to access the Yoda drive using WebDAV.

Note: if you are on Linux and comfortable with commandline tools, the [iRODS icommand](icommands.md) provides better performance.

## Create a config
Rclone always expects you to create a config first:
```
rclone config
Current remotes:

Name                 Type
====                 ====

e) Edit existing remote
n) New remote
d) Delete remote
r) Rename remote
c) Copy remote
s) Set configuration password
q) Quit config
e/n/d/r/c/s/q> n

Enter name for new remote.
name> yoda

Option Storage.
Type of storage to configure.
Choose a number from below, or type in your own value.

...
46 / WebDAV
\ (webdav)
...
Storage> 46

Option url.
URL of http host to connect to.
E.g. https://example.com.
Enter a value.
url> https://data.yoda.vu.nl

Option vendor.
Name of the WebDAV site/service/software you are using.
Choose a number from below, or type in your own value.
Press Enter to leave empty.
1 / Nextcloud
\ (nextcloud)
2 / Owncloud
\ (owncloud)
3 / Sharepoint Online, authenticated by Microsoft account
\ (sharepoint)
4 / Sharepoint with NTLM authentication, usually self-hosted or on-premises
\ (sharepoint-ntlm)
5 / Other site/service or software
\ (other)
vendor> 5

Option user.
User name.
In case NTLM authentication is used, the username should be in the format 'Domain\User'.
Enter a value. Press Enter to leave empty.
user> *****@vu.nl

Option pass.
Password.
Choose an alternative below. Press Enter for the default (n).
y) Yes, type in my own password
g) Generate random password
n) No, leave this optional password blank (default)
y/g/n> y
Enter the password:
password:
Confirm the password:
password:

Option bearer_token.
Bearer token instead of user/pass (e.g. a Macaroon).
Enter a value. Press Enter to leave empty.
bearer_token>

Edit advanced config?
y) Yes
n) No (default)
y/n> n

Options:
- type: webdav
- url: https://data.yoda.vu.nl
- vendor: other
- user: p.j.m.vos@vu.nl
- pass: *** ENCRYPTED ***
  Keep this "yoda" remote?
  y) Yes this is OK (default)
  e) Edit this remote
  d) Delete this remote
  y/e/d> y


Name                 Type
====                 ====
remote               onedrive
yoda                 webdav

e) Edit existing remote
n) New remote
d) Delete remote
r) Rename remote
s) Set configuration password
q) Quit config
e/n/d/r/c/s/q> q
```

## Mounting on Windows
Please make sure to use `--vfs-cache-mode`, see (rlone docs)[https://rclone.org/commands/rclone_mount/#vfs-file-caching]

```
.\rclone --vfs-cache-mode full mount yoda:research-staff-ubvu-geoplaza/ y:
```
Will mount the `yoda` config as drive Y.