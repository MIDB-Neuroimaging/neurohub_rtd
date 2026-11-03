# Importing Scan Protocols at the Console
Researchers often share scan protocols so that the exact same sequences can be run at different scanners. To do this on the 3T-D XA60 console you will need:

- An exar1 file of the scan protocol to import
- The exar1 file saved on a Windows-formatted thumb drive

An exar1 is the file type that stores scan protocol information in the Siemens Syngo environment. The Syngo software operates on a Windows machine and the thumb drive must be compatible (e.g., ex-FAT, NTFS). 

Follow these steps to import a scan protocol:

1. Verify that your thumb drive has the correct exar1 file. This file cannot be opened on the average computer.
2. Reserve ~30 minutes time on the scanner under your project.
3. Plug your flash drive into the console computer tower. At 3T-D, this computer is under the desk where the scan operator sits, near the sink.
4. On the home screen, click “My Exam Cockpit" > Select > Import > From existing file > Import.
5. Browse the file exporer and choose the exar1 file from your flash drive. Click “open".
6. In the protocol tree on the left side of the window, select the folder where you would like to save the new protocol. If you would like to make a sub-folder, you can do so by right-clicking and choosing that option.
7. Click the left arrow button in the center of the screen (<<) to import the scan protocol. A new window will show the import progress and any errors that may have occurred.
8. To rename your protocol, right-click on it and choose “rename”.
9. Your protocol has been imported! You should be able to click into it and see the new sequences.
10. In the MyExam Cockpit import tab, close the internal window showing the flash drive files and eject the thumb drive. Double check your work by mock-registering a participant and selecting your new protocol. 

IF YOUR PROTOCOL DOES NOT TRANSFER AT STEP 7: 

You may have portions of  your protocol that are not compatible with the scanner. If some of your sequences appear to be greyed out, you may run into this issue. If you attempt to import an incompatible scan, an error may pop up while importing, notifying you.
- Click the drop down arrow near the folder icon at the top left of the screen, near “user” 
- Click “show inconsistencies”. This will show any protocols containing sequences that are not compatible with the scanner and the incompatible sequences within those protocols.
- Navigate to the Program Editor, open the protocol and delete the incompatible sequence (greyed out).
- Your protocol should now be visible from the protocol browser! You should be able to open it, see the different sequences, and load it when registering a patient.
