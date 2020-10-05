# ABOUT
This small script can be used to receive a telegram message when a user logs in via SSH.

# 1. Create a Bot
1.1 add @BotFather at telegram
1.2 send `/newbot`
1.3 follow the instructions
1.4 copy the generated token, looks like `1176193427:TFGUxf0qeRUHiDFVedfeDiW3MyoEFFf99B_I8`

# 2. Get you Chat ID
2.1 Write a message to your created Bot (URL to your bot is provided at the BotFather chat)
2.2 check the following URL
`https://api.telegram.org/bot{bot_token}/getUpdates`
2.3 the ID is at
`"message":{"message_id":1,"from":{"id":{YOUR CHAT ID},"is_bot":false [...]`

# INSTALL
Clone the repository:
`git clone R60olus/ssh-telegram-alert`

Edit telegram.sh
`nano telegram.sh`

set your CHAT und BOT ID
`CHAT_ID=XXX
BOT_TOKEN=XXX`

should look like:

`CHAT_ID={YOUR CHAT ID}
BOT_TOKEN={YOUR BOT TOKEN}`

copy the file at `/etc/profil.d/`

`cp telegram.sh /etc/profil.d/telegram.sh`

make ist runable

`chmod +x /etc/profil.d/telegram.sh`

# Test
Test the script, yust login with a user.
You should now get a message via telegram like:

`New SSH login
Server: myserver.myserver.de
User: root
IP: 123.34.34.2
Country: Germany
Date: 14:20:40, 05.10.2020

# Have fun
