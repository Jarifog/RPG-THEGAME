# BUGLOG

Name: 

## Bug #1
#ifndef CHARACTER_H_
instead of 
#ifndef CHARACTER_H
(Missed underscore)
## Bug #2
while (hero.isAlive() && monster.isAlive()) 
instead of
while (hero.isAlive() || monster.isAlive()) 
(Should be And instead of OR)
## Bug #3
void drinkPotion(Character &hero) 
instead of 
void drinkPotion(Character hero) 
(Pass by reference instead of pass by copy)
## Bug #4 
hero.hp += 10;
if (hero.hp > hero.maxHp) {
    hero.hp = hero.maxHp;
}
instead of 
hero.hp += 10;
(Increase max hp if current hp healed more than current hp)
## Bug #5
for (int i = 0; i < 3; i++) 
instead of 
for (int i = 0; i <= 3; i++) 
## Bug #6
return Character(names[pick], hps[pick], atks[pick], defs[pick]);
instead of 
return Character(names[pick], atks[pick], hps[pick], defs[pick]);