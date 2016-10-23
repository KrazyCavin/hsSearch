---
Title: hsSearcher
Description: look up Hearthstone cards in terminal
Author: KrazyCavin
Tags: CLI, python, script
created:  04 Sep 2016
---

hsSearcher
==========
Show Hearthstone cards information in CLI. All cards data are collected from http://www.hearthhead.com/

### Requirement
* Python3
* texttable

### Install python package
* pip install texttable

### How to use
```
usage: hsSearch.py [-h] [-a [ATTACK [ATTACK ...]]] [-l [LIFE [LIFE ...]]]
                   [-t [TEXT [TEXT ...]]]
                   [-tp [{minon,spell,weapon} [{minon,spell,weapon} ...]]]
                   [-m [{0,1,2,3,4,5,6,7} [{0,1,2,3,4,5,6,7} ...]]]
                   [-f [{standard,wild} [{standard,wild} ...]]]
                   [-s [{basic,classic,kara,og,tgt,loe,brm,gvg,naxx} [{basic,classic,kara,og,tgt,loe,brm,gvg,naxx} ...]]]
                   [-r [{dragon,mech,totem,demon,pirate,murloc,beast} [{dragon,mech,totem,demon,pirate,murloc,beast} ...]]]
                   [-rr [{free,common,rare,epic,legendary} [{free,common,rare,epic,legendary} ...]]]
                   [-c [{neutral,warrior,priest,hunter,rogue,paladin,shaman,mage,warlock,druid} [{neutral,warrior,priest,hunter,rogue,paladin,shaman,mage,warlock,druid} ...]]]
                   [-d]
                   [name [name ...]]

positional arguments:
  name                  search text

optional arguments:
  -h, --help            show this help message and exit
  -a [ATTACK ...], --attack [ATTACK ...]
                        filter attack value
  -l [LIFE ...], --life [LIFE ...]
                        filter life value
  -t [TEXT ...], --text [TEXT ...]
                        card description
  -tp [{minon,spell,weapon} ...], --type [{minon,spell,weapon} ...]
                        card type
  -m [{0,1,2,3,4,5,6,7} ...], --mana [{0,1,2,3,4,5,6,7} ...]
                        filter mana
  -f [{standard,wild} ...], --format [{standard,wild} ...]
                        card set fromat: wild or standard
  -s [{basic,classic,kara,og,tgt,loe,brm,gvg,naxx} ...], --set [{basic,classic,kara,og,tgt,loe,brm,gvg,naxx} ...]
                        card set
  -r [{dragon,mech,totem,demon,pirate,murloc,beast} [{dragon,mech,totem,demon,pirate,murloc,beast} ...]], --race [{dragon,mech,totem,demon,pirate,murloc,beast} [{dragon,mech,totem,demon,pirate,murloc,beast} ...]]
  -rr [{free,common,rare,epic,legendary} ...]], --rarity [{free,common,rare,epic,legendary} ...]
                        filter by card rarity
  -c [{neutral,warrior,priest,hunter,rogue,paladin,shaman,mage,warlock,druid} ...], --class [{neutral,warrior,priest,hunter,rogue,paladin,shaman,mage,warlock,druid} ...]
                        filter by class
  -d, --debug           active debug log
```

### Example
* List **Overload Epic** cards: ```hsSearch.py Overload -rr epic```
![Alt text](https://github.com/KrazyCavin/hsSearch/blob/master/example/usage1.png "use case 1")

* List **0 cost Mage** card: ```hsSearch.py -m 0 -c Mage```
![Alt text](https://github.com/KrazyCavin/hsSearch/blob/master/example/usage2.png "use case 2")

* List **12 Attack** point cards: ```hsSearch.py -a 12```
![Alt text](https://github.com/KrazyCavin/hsSearch/blob/master/example/usage3.png "use case 3")

* List **Medivh** card wiht **Neutral** class: ```hsSearch.py medivh -c neutral```
![Alt text](https://github.com/KrazyCavin/hsSearch/blob/master/example/usage4.png "use case 4")
