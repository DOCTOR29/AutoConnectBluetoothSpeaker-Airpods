
open ~/living_room_speaker_connect.app ======place in home as rename living_room_speaker_connect.app
Install sleepwatcher => brew install sleepwatcher
At first create => ~/.wakeup and ~/.sleep scripts and put some shell logic into it
Add necessary permissions => chmod 700 ~/.sleep && chmod 700 ~/.wakeup
Test it locally => /usr/local/sbin/sleepwatcher --verbose -w ~/.wakeup - go to sleep with running terminal

sudo ln -sfv /usr/local/Cellar/sleepwatcher/2.2.1/homebrew.mxcl.sleepwatcher.plist /Library/LaunchAgents/
Load launchd task => sudo launchctl load /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist

sudo chown root:wheel /Users/naveedislam/Library/LaunchAgents/homebrew.mxcl.sleepwatcher.plist

