# Navigating to Naxos

## Naxos
Data exported from CMRR scanners are usually pushed to the naxos node. Naxos is the dicom reciever hosted by CMRR. To access data on naxos, you must:

1. be a registered user of CMRR 
2. have access to CMRR's VPN 
3. have basic knowledge of the command line

!!! note
    If you don't have CMRR access yet or are not sure if you have VPN access, follow the instructions here. 

!!! note
    If you don't know how to use the command line yet or need a refresher, check out the [Unix tutorial](https://andysbrainbook.readthedocs.io/en/latest/unix/Unix_Intro.html){:target="_blank"} at Andy's Brain Book. 

## Navigating to naxos

1. Connect to the CMRR VPN. Use your UMN username and password. 
2. Open a web browser and navigate to [https://login2.cmrr.umn.edu/.](https://login2.cmrr.umn.edu/){:target="_blank"}{:target="_blank"} This will open an NX client. 
3. Use your CMRR username and CMRR password. 
4. Open a new virtual desktop and click "OK" through to the remote desktop. 
5. Click "Activities" then click on the Terminal icon to open a terminal. 
6. Navigate to the naxos directory. 

`cd /home/naxos2-raid2/dicom/`

6. If you type `ls` and press enter, you'll see the list of every scan that has been recently exported from CMRR scanners. Search for your data by Scan Date and the Last Name entry from your scanning session. 

!!! tip
    Confirm that all of your data was successfully transferred

    `find dateofscan-STXXX-lastname -type f | wc -l`

    This number should match the number of instances that were sent from the scanner computer. 

If needed, more detail can be found in the [CMRR documentation](https://www.cmrr.umn.edu/computeruser/nc-cms/content/upload/C104-05%20-%20Connecting%20Macs%20to%20CMRR%20servers%20with%20NX%201.4.pdf){:target="_blank"} on connecting to naxos. 
