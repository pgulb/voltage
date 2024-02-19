# VoltageWare  
  
CLI-driven game surival-rpg-roguelike-something with cloud backend  
  
## TODO  
- user api  
- worker  
- user client  
- ttyd docker deployment on frog  
  
- NO mongo api  
- NO rabbitmq api  
  
## Features
  
### client
- browsing of user's current stats/items etc
- pull default .rc from repo
  
### client config
- store client config in ~/config/.voltagerc or something  
- encrypt username and password with 4 digit PIN using AES  
- store there locale setting [pl/en]  
- store API URL  
- store terminal color settings  
  
### API  
- basic auth with mongo backend  
- checking status if event lock  
- downloading current user state  
- posting user events  
- registering users into mongo  
- putting events to rabbitmq  
  
### worker  
- get events off queue  
- process events  
- validate events  
- put processed events on 'response' queue for api to grab  
  