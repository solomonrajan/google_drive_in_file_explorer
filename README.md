# google_drive_in_file_explorer

Enables Google Drive for Desktop to show in Windows File Explorer, same as the way that OneDrive or DropBox does!

OneDrive and Dropbox both create non-removable shortcuts in the Windows Explorer sidebar - the same unfortunately cannot be said for Google Drive. The Scripts and Registry in this repository will make the necessary changes to allow for a Google Drive shortcut in Windows Explorer. The original article can be found at [Adding Google Drive to the Windows Explorer sidebar](https://luke.digital/adding-google-drive-to-the-explorer-sidebar/)

**Disclaimer: This was tested on Windows 11 Professional, Windows 10 Professional and Windows 8.1 Professional. Ensure you backup your registry before making any changes.**

## Installation

1. Clone this repository.
2. Open  **enable_google_drive.reg**  in your favourite text editor.
3. Update references of DefaultIcon in line #32 & #48  `@="C:\\Program Files\\Google\\Drive File Stream\\xx.x.x.x\\GoogleDriveFS.exe,0"` to location you've installed Google Drive, keeping ",0" at the end of the drive path.
4. Update any references of "TargetFolderPath"=`"G:\\\My Drive"` to location you have configured Google Drive to store files.
5. Save all changes.
6. Double-click  **enable_google_drive.reg**  to install and ensure you click "Yes" when prompted by UAC.

   `To stop the drive icon reverting to default when Google Drive File Stream updates, create a backup copy of GoogleDriveFS.exe in a safe location (e.g C:\Backups) and update any references of @="C:\\\Program Files\\\Google\\\Drive File Stream\\\xx.x.x.x\\\GoogleDriveFS.exe,0" to this location instead. This is because this folder is deleted occasionally when Google updates their software.`

## Credits

Original work by [**Svenkle Github**](https://github.com/svenkle/google-drive-add-to-explorer/)
