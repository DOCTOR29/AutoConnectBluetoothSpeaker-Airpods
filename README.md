# AutoConnectBTSpeaker/airpods On MacOS Ventura/moneterey
 
0. Download the release app and extract it
1. open content of living_room_speaker_connect.app by command+clicking it and navigate to open file /living_room_speaker_connect.app/Contents/Resources/Scripts/main.scpt
 
2. In the main.scpt file change "Living room speaker" to speaker name or Airpods name and save it
3. place in home rename as living_room_speaker_connect.app
4. make a file .wakeup in home directory and paste the following command
5. open ~/living_room_speaker_connect.app 
6. install sleepwatcher => brew install sleepwatcher
7. need homebrew package manager for installing sleepwatcher

8. chmod 700 ~/.wakeup
Test it locally => /usr/local/sbin/sleepwatcher --verbose -w ~/.wakeup - go to sleep with running terminal

9. sudo ln -sfv /usr/local/Cellar/sleepwatcher/2.2.1/homebrew.mxcl.sleepwatcher.plist /Library/LaunchAgents/

10. sudo chown root:wheel /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist

11 .Load launchd task => sudo launchctl load /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist

