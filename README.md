# AutoConnectWifiSpeaker
 Auto Connect wifi speaker 
 
 open content of living_room_speaker_connect.app navigate  /living_room speaker_connect.app/Contents/Resources/Scripts/main.scpt
 change air
 change  to "Living room speaker" to speaker name and save it
place in home as rename living_room_speaker_connect.app
make a file .wakeup in home directory and paste the following command
open ~/living_room_speaker_connect.app 
Install sleepwatcher => brew install sleepwatcher

chmod 700 ~/.wakeup
Test it locally => /usr/local/sbin/sleepwatcher --verbose -w ~/.wakeup - go to sleep with running terminal

sudo ln -sfv /usr/local/Cellar/sleepwatcher/2.2.1/homebrew.mxcl.sleepwatcher.plist /Library/LaunchAgents/

sudo chown root:wheel /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist

Load launchd task => sudo launchctl load /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist

