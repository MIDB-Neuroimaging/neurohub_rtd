## Transfer from Naxos to Tier 2

We recommend using [rclone](https://github.com/rclone/rclone) to transfer data to Tier 2. Transfers to Tier 2 are faster, more secure, and does not impact Tier 1 quota. 

### Installation and setup:

1. Connect to CMRR servers with an NX client. 
2. Open a terminal. 
3. Navigate to your home directory.
`cd ~` 
4. Clone the rclone repo. 
`git clone https://github.com/rclone/rclone`

5. Time to set up a config file. 
`rclone config`

You will see a series of options. To set up a new config, type `n` and complete the following:

* Name: s3 (can be anything, but we're calling it s3)
* Storage: 4 (amazon s3)
* Provider: 3 (Ceph)
* env_auth: leave blank, press enter to continue

Next you'll be promted for your access_key_id and your secret_access_key which are specific to your umnID and can be located [here](https://www.msi.umn.edu/content/s3-credentials).

* region: leave blank and press enter to continue
* endpoint: s3.msi.umn.edu

The rest of the options can be left blank. Press enter to continue until you can quit out of the menu. 

### Usage

From /home/naxos2-raid2/dicom/:

`rclone copy --progress [folder] s3://[s3bucket]/dicoms/[folder]`

Example:
`rclone copy --progress 20230101-DATAFOLDER s3://mybucket/dicoms/DATAFOLDER`

!!! note
    The rclone "copy" command will make sure all files at the source match the destination and will not overwrite matching ones. 
    
!!! warning 
    You MUST specify a new folder (DATAFOLDER in the example above) to the destination because rclone will always copy CONTENTS of the directory rather than the directory itself. This actually works out because you should change the name of the dicom folder to strip the date. If the folder does not exist yet, rclone will make it for you.

!!! warning
    NO TRAILING SLASHES

!!! tip
    The progress flag is optional and shows the transfer progress. 

!!! danger
    NEVER USE 'rclone sync' command to copy files. When used incorrectly, it will DELETE files from the destination. 

!!! tip 
    If you are having trouble getting rclone to work try adding the path to your cshrc. 

    `gedit ~/.cshrc`
    
    Under #additions add the following:
    `setenv ${PATH}:/${HOME}/rclone`

## Transfer from Naxos to Tier 1

Use an scp command to transfer data folders to Tier 1. You will need to duo in so have your phone handy! 

`scp -o IdentitiesOnly=yes -r dataFolder umnID@mesabi.umn.edu:/home/MSIshare/umnID/`

!!! tip 
    Leave the trailing slash off your dataFolder

!!! tip 
    Transfer data to your home directory rather than a shared directory on Tier 1. MSI is a little fussy about transfers from remote servers and I have had fewer hiccups when transferring to my home directory. 