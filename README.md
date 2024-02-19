# VoltageWare  
  
CLI-driven game surival-rpg-roguelike-something with cloud backend  
  
## TODO  
- user api  
- worker  
- user client  
- ttyd docker deployment on frog  
- possible discord bot integration  
  
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
  
### game mechanics  
- % of body parts health  
- % of blood level  
- bleeding as % of max blood per turn  
- % of sanity affecting encounters and fights, death at 0
- poison as turns to death  
- confusion as 30% chance to do random action  
- burn damage deal damage to affected body part, each burn can spread to other part  
- paralyze as 20% chance to skip turn  
- curse lowers attack damage to 80%  
- nuclear fallout - damage to all body parts and sanity, more as environmental hazard  
