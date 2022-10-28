# AutoConnectBTSpeaker/airpods On MacOS Ventura/moneterey
AutoConnectBTSpeaker/airpods On Startup and after wake up from sleep
 
 
	•	 Download the release app and extract it
	•	 open  system settings>General>login Items> open at login and select living_room_speaker_connect.app from extracted zip file
	•	 open content of living_room_speaker_connect.app by command+clicking it and navigate to open file /living_room_speaker_connect.app/Contents/Resources/Scripts/main.scpt
	•	 In the main.scpt file change "Living room speaker" to speaker name or Airpods name and save it
	•	 place in home rename as living_room_speaker_connect.app
	•	 make a file .wakeup in home directory and paste the following command
	•	 open ~/living_room_speaker_connect.app 
	•	 install sleepwatcher => run brew install sleepwatcher
	•	 need homebrew package manager for installing sleepwatcher
	•	 run chmod 700 ~/.wakeup
	•	Test it locally => /usr/local/sbin/sleepwatcher --verbose -w ~/.wakeup - go to sleep with running terminal
	•	run sudo ln -sfv /usr/local/Cellar/sleepwatcher/2.2.1/homebrew.mxcl.sleepwatcher.plist /Library/LaunchAgents/
	•	run  sudo chown root:wheel /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist
	•	Load launchd task => run sudo launchctl load /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist
