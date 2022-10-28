# AutoConnectBTSpeaker/airpods On MacOS Ventura/moneterey
AutoConnectBTSpeaker/airpods On Startup and after wake up from sleep
 
1.Download the release app and extract it

2.open  system settings>General>login Items> open at login 
and select living_room_speaker_speaker_connect.app from extracted zip file
3. open content of living_room_speaker_connect.app by command+clicking it and navigate to open file /living_room_speaker_connect.app/Contents/Resources/Scripts/main.scpt
4.	 
5.In the main.scpt file change "Living room speaker" to speaker name or Airpods name and save it
6. place in home rename as living_room_speaker_connect.app
7. make a file .wakeup in home directory and paste the following command
8.open ~/living_room_speaker_connect.app 
9.install sleepwatcher => brew install sleepwatcher
10.need homebrew package manager for installing sleepwatcher
	
11.chmod 700 ~/.wakeup
12.Test it locally => /usr/local/sbin/sleepwatcher --verbose -w ~/.wakeup - go to sleep with running terminal
	
13.sudo ln -sfv /usr/local/Cellar/sleepwatcher/2.2.1/homebrew.mxcl.sleepwatcher.plist /Library/LaunchAgents/
	
14sudo chown root:wheel /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist
	
15.Load launchd task => sudo launchctl load /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist
	
