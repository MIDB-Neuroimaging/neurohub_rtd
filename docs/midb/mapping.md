# Connecting to a CMRR server on 3T-D
This SOP outlines how to map to a CMRR server (i.e. Naxos) from the 3T-D console computer. This is necessary if you need to re-import a scan that was removed from the computer. 

## Map to the Network Drive
!!! tip
    <mark>Highlighted instructions</mark> are the one that worked most recently, but another combination of options may work for you! This is a finicky process!
1. Ctrl + Esc -> File Explorer
2. Right click on “this PC” and select “map to a network drive”
    - Drive to map: 
        - <mark>\\range1.cmrr.umn.edu\dicom</mark>
        or
        - <mark>\\range1.cmrr.umn.edu\CMRRusername</mark>
    - Check the box for “use different credentials”
    - Click “finish”
    -  You’ll be prompted for your CMRR username and password
        - Username: 
            - cmrr\CMRRusername
            or
            - <mark>CMRRusername@cmrr.umn.edu</mark>
        - Password: CMRR password
3. If successful, you will now see the file tree of scans on Naxos, organized by month/year

## Importing a Scan
1. Back in the scanner system, open up the patient browser
2. Select ‘Import’
3. Your CMRR drive will show up as an option - navigate through the files and find the scan you want
4. Select ‘Import’ 
5. Your scan will now appear in the patient browser (note: expect the import to take the same amount of time as the original export to naxos took)

## Burning to Disc
1. Plug in CD burner to host computer
2. Insert CD (located on shelf above Mac)
3. Export


## CMRR Reference Docs
- [PC](https://www.cmrr.umn.edu/computeruser/nc-cms/content/upload/C103-02-ConnectingPCstoCMRRserverfileshares1.2.){:target="_blank"}pdf  
- [Mac](https://www.cmrr.umn.edu/computeruser/nc-cms/content/upload/C104-01-ConnectingyourMactotheCMRRnetwork1.3.pdf){:target="_blank"} 

