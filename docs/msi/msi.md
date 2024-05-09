# The Minnesota Supercomputing Institute

*The [Minnesota Supercomputing Institute](https://www.msi.umn.edu/){:target="_blank"} (MSI) provides the software, hardware, storage and experts to support research projects in all research areas.*

## Registering for Access

### UMN Employees

All UMN employees will have access to the MSI. 

PIs can request the activation of their share partition [here.](https://www.msi.umn.edu/access){:target="_blank"} Your share partition will be named your umnID. 

### Non-UMN Employees

In order to request an MSI account as a non-UMN employee, a Person of Interest (POI) account must first be created. Non-UMN users will need written support from a UMN PI. Follow the instructions [here.](https://www.msi.umn.edu/support/faq/how-do-i-get-person-interest-poi-designation){:target="_blank"}


## Gaining Access to MSI


### Establish VPN

To remotely log into MSI you need to establish a VPN connection. Detailed instructions can be found on [HST/AHC: VPN and Remote Desktop Setup](https://it.umn.edu/services-technologies/how-tos/hstahc-vpn-remote-desktop-setup){:target="_blank"} for Windows, OS X, and Linux.

!!! note
	If you already have VPN on your computer for another institution, you will need to complete the following steps:

1. Type "tc-vpn-1.umn.edu" in the box
2. Choose "anyconnect-UofMvpnfull" from the group
3. Enter your username and password

*This installs required setups for VPN, after which you will have a dropdown with UMN choices and you can use "split tunnel" moving forward.*

*If you receive an error message the first time, simply re-open Cisco.*

### Permissions

!!! warning 
	Important!
	To ensure the data and code created can be accessed by any user on the share partition, update your bashrc with the following steps (this only needs to be done the first time you access MSI). See here for some info on what a "[bashrc](https://www.journaldev.com/41479/bashrc-file-in-linux){:target="_blank"}" is.

1.  Open your bashrc file with a text editor, e.g. `emacs ~/.bashrc`.
2.  Set `umask` to `0007`. The `umask` is the default permission (self, group, like `faird`, and all users can be given read, write, and execute access) applied to the files you create. `0007` gives read, write, and execute access to you and all group members, but no one else (this could be anyone in the university). See [here](https://wintelguy.com/umask-calc.pl){:target="_blank"} for details.
3.  Close the file and type `source ~/.bashrc` into the terminal to apply the changes.
4.  Your bashrc is loaded each time you log in, so you only need to `source` it when you edit it mid-session.

## Delays and Problems

If you experience delays or problems accessing the MSI or a particular node, the reason could be that the MSI might be non-fully operational at that time. The first Wednesday of each month the system is down for maintenance. Use the following links to check the MSI system and node status at any time:

- [MSI System status](https://status.msi.umn.edu/){:target="_blank"}
- [MSI node status](https://umgcdownload.msi.umn.edu/website/slurmnodes/index.html){:target="_blank"}
