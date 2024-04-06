# Voltage  
  
CLI-based game surival-rpg-roguelike-something with cloud backend  
  
## TODO  
https://github.com/users/pgulb/projects/1/views/1  
  
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
- using websockets to communicate game events  
  
### worker  
- get events off queue  
- process events  
- validate events  
- put processed events on 'response' queue for api to grab  
  
### game mechanics  
- % of body parts health  
- % of rust/burn of parts  
- nuclear fallout - damage to all body parts  
- rust from water/rain  
- rust affecting health loss/hit durability of part  
- using cola to unrust parts  