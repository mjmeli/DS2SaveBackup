Dark Souls II Automatic Save Backup
=============

##### Description
This is the source code for my Dark Souls II Automatic Save Backup program. This is written in C# targetting .NET 4.5.

I created this program primarily for myself. I have been using other programs, but have wanted a program with a GUI interface that has a few more elaborate features than simply copying files from one directory to another. As such, I made this.

##### Key Features
Compared to other DS2 save backup programs, this has all of the standard plus a few unique features:

* GUI!
* Automatic save directory detection
* Customizable backup frequency (in minutes)
* Backup file size tracking
* Easy way to manually clear out all existing backups
* Optional automatic cleanup of old backups (in terms of number of backups kept)
* Support for multiple save files
* Instant backup option when you need a quick backup
* Instant restore option, which will replace your saves with your most recent backups

##### Code Overview
The main program is handled through DS2SaveBackup.cs. This class operates the GUI and manipulates/coordinates the backup and save files.

The helper classes SaveLoc and BackupLoc are used by the program to manage save and backup locations. The classes hold information about where the save and backups are kept, how many backups have been performed, the total size of the backups, and of course the actual save files themselves. Each class has helper methods as well obviously.

The save files are tracked as instances of the SaveFile class. These objects will keep track of how many times they each have been backed up, what their earliest backup is, what their latest backup is, and other things.

While the general idea of this program is that it simply copies files from the save directory into the backup directory at fixed intervals, this seemingly more complex than necessary code structure allows me to implement the other features such as automatic backup cleanup, instant restore, and persistent backup after closing/opening the program multiple times.

##### Bugs/Comments
If you come across any bugs (and there should be plenty!) or have comments, especially feature suggestions, feel free to contact me (info below). I managed to implement everything that I needed to the level I wanted, but I am more than willing to extend what I have for other people.

Contact:
  Email: mjmeli94@gmail.com
  Reddit: /u/Hurricane043
