# Connecting to the Yoda Network Disk on Linux

## Using GNOME Files

GNOME users can connect to the Yoda Network Disk with GNOME Files (also known as Nautilus in older versions of GNOME).

![alt text](screenshots/linux-connect-to-server.png "GNOME Files screenshot")

Click on "+Other Locations" and enter the server address in the "Connect to Server" bar.

| Environment          | Address | Remarks                  |
|:-------------------- |:------------|:-------------------------|
| AIMMS pilot | https://data.aimms.labs.vu.nl/ | |
| Surf Yoda pilots | https://vu-data.irodspoc-sara.surf-hosted.nl/ | |

Then click on the Connect button.

![alt text](screenshots/linux-enter-password.png "GNOME Files password dialog screenshot")

You will be prompted for a name and password.
If you are an employee or student at Utrecht University, your user name is your Utrecht University email address (in lowercase) and your password
is your Solis password.  External users have usually received their user name via email, along with a link to set their password.

## Using command line tools

If you prefer to use command line tools, you can use these methods:
- Mount the Yoda Network Disk as a davfs volume. You may need to install a davfs package on your system first. On Debian-based systems, such as Ubuntu: _apt install davfs2_, and answer "Yes" to the question about allowing regular users to mount WebDAV volumes. On RedHat-based systems, such as CentOS or Fedora: _yum install davfs2_. Now look up the server address of your environment in the table above.  Replace the "davs://" in the server address with "https://" when entering the mount command. For example: _mount -t davfs https://data.aimms.labs.vu.nl/ /mnt_.  
Important: Ensure that in the configuration file _/etc/davfs2/davfs2.conf_ the parameter "delay_upload" has the value "0" (zero) which may be different from the default. This avoids data loss from failure-to-flush-data issues on larger file transfers. With credits to [Joost de Graaf](https://www.uu.nl/medewerkers/JdeGraaf) for reporting this solution.
- [The Cadaver commandline WebDAV client](http://www.webdav.org/cadaver/) is also compatible with the Yoda Network Disk.
