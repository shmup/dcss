# Dungeon Crawl Stone Soup

[Dungeon Crawl Stone Soup](https://en.wikipedia.org/wiki/Dungeon_Crawl_Stone_Soup) is a [roguelike](https://en.wikipedia.org/wiki/Roguelike) where the player creates a character and guides it through a diverse branching dungeon, full of monsters and items, with the goal of retrieving at least 3 of the 15 "runes of Zot", fetching the Orb of Zot, and escaping alive.

_rng [giveth](http://i.imgur.com/XV18fWm); rng [taketh](http://i.imgur.com/EQgGwVt)_

## Contents
 - [Useful Commands](#useful-commands)
 - [Useful Config Settings](#useful-config-settings)
 - [Formulas](#formulas)
 - **Mini Guides**
    * [Where Should I Go Next](#where-should-i-go-next)
    * [Killhole](#killhole)
    * [How do I stop dying in the Abyss every time I get to the mid game?](#how-do-i-stop-dying-in-the-abyss-every-time-i-get-to-the-mid-game)
    * [What weapon should I use?](#what-weapon-should-i-use)
        - [A quick guide to brands](#a-quick-guide-to-brands)
        - [Weapon Types](#weapon-types)
    * [Patashu's Tips](#patashus-tips)
 - [Bot Commands](#bot-commands)
 - [Links](#links)

### Useful Commands
key                 | action
----                | ----
??                  | a list that details all of the following bindings, and more!
o                   | autoexplore (stops at first site of various things: monsters, doors, items, etc)
tab                 | autofight (moves you towards enemy, too. press **shift-tab** to stand still)
shift+direction     | moves you all the way in said direction until 'disturbed' (see something)
ctrl+x              | shows a list of visible monsters with armour and weapon included in description
ctrl+o              | show which branches you could/have visit and what depths you've seen
shift-g             | travel between dungeons
ctrl-f              | search for drops. i like to 'search armour, search shield, search gift, search artif, etc (useful because you very probably miss drops sometimes. i use this feature often. you should too!
( and ) when firing | changes ammo type. less error prone than selecting by letter
f.                  | fire at target but don't let ammo go past them if misses. useful in cases of friendlies/lava/water
ff                  | fire at last target
'                   | swaps between weapons in inventory slot "a" and "b"
=                   | can reassign inventory slot item letters. useful for swap weapons
\                   | toggle autopickup status of items you've already recognized
~                   | use macros. great for magic users. imagine your number row as a spell bar.
shift-x then e      | makes an area excempt from autoexplore. double tap e to select a single tile


### Useful Config Settings
setting                      | result
--------                     | --------
autofight_stop=60            | HP thresholds for refusing to autofight
default_manual_training=true | essential, IMO, since autoskilling is generally way worse. It just selects manual skilling mode as the default (so you don't have to .. manually.. switch to it every new character.)
easy_eat_chunks=true         | you won't be prompted whether to eat chunks (unless they are 'bad quality' -- what used to be 'contaminated' and may still be if you are playing an old version of DCSS.)
explore_delay=-1             | makes autoexplore not update the display until it stops (so it is as fast as possible). travel_delay=-1 | is similar for travelling.
hp_warning=50                | Low-HP warning
pickup_mode=multi            | a menu of items on ground that you toggle + or - to pickup. much more useful
show_travel_trail=true       | shows the path that was most recently taken by autoexplore. Particularly useful if you are using explore_delay=-1 described above.

### Formulas
             | formula
------       | --------
weapon level | (base attack delay - minimum delay) * 20

## Where Should I Go Next?
Here's my branch order, which I think is fairly common. There are times when deviating from this branch order is a good idea, mostly if you encounter something extremely nasty in the branch you're trying to clear and can't go around it.

1. Clear dungeon until I find Lair.

2. Clear Lair (some people like to save Lair 8, or at least the Lair 8 treasure Vault, for later. This is reasonable, although most characters can manage it right away if they're careful).

3. If I haven't found it yet, keep clearing dungeon until I find the Orcish Mines.

4. Clear Orcish Mines (the same thing I said about Lair 8 applies to Orc 4, although the jump in difficult from Orc 3 to Orc 4 is usually much bigger than the jump from Lair 7 to Lair 8, so be careful).

5. Finish clearing the dungeon.

6. Clear the first four floors of either Snake or Spider, whichever I have.

7. Clear the first four floors of either Swamp or Shoals, whichever I have. (Swamp and Shoals are comparable in difficulty to Snake or Spider, so steps 6 and 7 can be switched, especially if you're missing rPois, but for most characters I find Snake and Spider easier than Swamp and Shoals)

8. Clear floor 5 of either Snake/Spider or Swamp/Shoals, whichever I found easier, and get the rune.

9. Clear Vaults 1-4. Stay away from Vaults 5.

10. If I want some more loot or experience, clear Crypt. If you're planning to get more than 5 runes and want to switch to the Shining One later, save Crypt for piety (don't bother with the Shining One if you don't plan to get more than 5 runes).

11. If I still want more loot or experience, clear Elf. Elf 3 vault is extremely dangerous, be very careful there, it's much, much harder than the rest of Elf. I recommend using killholes there. I'll probably make a post about killholes in this thread at some point or other. Many very good players will advise you to never bother clearing elf at all, the risk of dying is often not worth it, so be careful here and I'd probably stay away if you haven't won before.

12. Clear Depths.

13. Get the other rune from Snake/Spider/Swamp/Shoals. This can be done earlier if you want. But do it now if you haven't yet.

14. Get my third rune. For 99% of characters this will be either Vaults, Slime, or Abyss. Usually Vaults, but sometimes I'll do Slime or Abyss if I think my characters is better suited for those (good stealth and ways of regenerating health and mana are great for Abyss, resist corrosion and mutation are important for Slime). If your character is undead, can cast necromutation, or worships Kiku, then Tomb can also be a choice for your third rune (although Tomb is getting new enemies in 0.16, one of which can cast dispel undead, so it will become much trickier and much more dangerous to undead and necromutation-users if you play there). I don't think I'd ever go to Pan or Hell for my third rune.

15. If I want to win with 3 runes, do Zot and Win. If I want more runes, I'll usually do Zot 1-4, Abyss, and Slime in some order, varying by character. I've done the switch to the Shining One once, and in that case I did Slime first before switching, then switched, then did Crypt for piety, Zot 1-4 to finish burning off my penance, and then Abyss. If I have no corrosion resistance, I'll avoid slime, it's crazy dangerous there without it.

16. If going for 5 or less runes, then you should have won by now. Otherwise, I'll usually do Pandemonium next, unless I'm a character well-suited for Tomb (Kiku worshipper, undead, or can cast necromutation).

17. After Pan, I'll usually do Tomb if I haven't yet, although some people like Saving Tomb for last. It can be a pain, and there's a lot of rotting and stat drain there, which is annoying.

18. The Hells are last. My standard order for the Hells is Tartarus, Cocytus, Dis, Gehenna, I think that's often the order of difficulty, but it can vary by character.

19. By now, you should have 15 runes. Go and win. Unless you want to do a Ziggurat. I've never finished a Ziggurat, so I can't help you there.


## Killhole
This is a good trick for dealing with large swarms of enemies if you're in a branch with rock (diggable) walls and have wands of disintegration and/or digging (or you're a formicid - I recommend digging killholes all the time on a formicid). It's particularly amazing for dealing with elf 3 - the vault can honestly become less than half as dangerous if you dig a killhole by the entrance.
The idea is to dig a little zig-zag tunnel like this (the . are empty spaces, the x's are walls, and the @ is you):

```
x x x x
. x @ x
x . x x
x x x x
```

While you're in this tunnel, the only visible space is the space right next to you. This means that only one enemy will be in sight at a time. This means that you can fight enemies in this tunnel one at a time, without having to worry about ranged attacks, smite-targeted attacks, or summons from any of their friends.

If you've got a lot of nasty enemies coming in on you, or you're about to face a vault filled with ranged and smiting enemies iike the Elf vault, dig a killhole, get someone's attention, then go hide in the back and kill whoever comes. Repeat until everything's dead.

## How do I stop dying in the Abyss every time I get to the mid game?

**Not getting banished.**

The best way to avoid dying in the Abyss is to not get banished. There are two main sources of banishment - the spell, and enemies wielding distortion weapons.

For the spell, know which enemies cast the spell - some of the more common threats here are Deep Elf Sorcerers, Ogre Mages, Liches, and Wizards, but there are more. When you see one of these enemies, equip as much Magic Resistance as possible, it will reduce the odds of the spell succeeding (just wearing rings of magic resistance while wandering around is often a good idea). If you worship Trog, use Trog's hand. Now, spend as few turns in line of fire as the banisher as possible. If you can kill them quickly, do so. If not (for example, you're mostly a melee character and they're at a distance), try to reposition yourself so that you're either out of their sight, or have an ally or another enemy blocking their line of fire (for example, against ogre packs, try to get other ogres in between you and the mages). If possible, don't spend any turns in line of fire of a banisher but not attacking them.

Distortion is harder. Keep an eye out in your messages for the signs of a distortion weapon - if you see a message about space bending or distorting around an enemy, then they're wielding a distortion weapon. If you or an ally teleports or blinks when hit by an enemy, they're probably wielding a distortion weapon. Sonja will also very frequently have a distortion weapon. If an enemy has a distortion weapon, do whatever possible to not fight them in melee. Any hit could banish you. If you really want to be careful, don't get into melee fights with any enemy with an unidentified glowing weapon, but this can be a massive hassle and distortion weapons are quite rare.

**Escaping the Abyss**

Of course, sometimes these method fail and you'll end up in the Abyss. So now what? It's a common misconception that getting banished in is a guaranteed death sentence or a matter of luck. It's very escapable by most characters, you just have to handle it properly. [Here is an excellent Tavern post on what to do once you end up in the Abyss](https://crawl.develz.org/tavern/viewtopic.php?f=5&t=11724&p=163927&hilit=abyss#p163927).

Basically, don't fight any enemy unless you absolutely have to, cover as much ground as possible (the more tiles you reveal, the more likely one will contain the exit), and don't hesitate to use consumables like teleport or haste if you need to. And, if possible, avoid resting. If you've got any forms of channeling or regeneration, don't hesitate to use them.

Also, if you have a ring of teleportation, it can be quite effective to just randomly teleport until you end up within sight of an exit.

## AC versus Resistances (OR: AC works against most damage, not just physical)

This one's a common misconception. I see a lot of players putting too high a priority on resistances and not enough on AC. One thing I often discover is that many players assume that AC only works against physical damage, so resistances are necessary to protect yourself against enemy spells.

This is not the case. AC works against nearly everything. Offhand, the things I can think of that it won't help against are torment, hellfire, freeze, the cold component of ice fiend or simulacrum melee attacks, and the poison status effect, although there's probably more I'm forgetting.

Another important thing to note is how multi-pip resistances (fire, cold, and negative energy) work. The first pip is much more potent than the others. For fire and cold, the first pip is 50% damage resistance, the second is 66%, and the third is 80% (I may have these numbers wrong). For negative energy, I forget the exact numbers, but I know the third pip gives complete immunity. In either case, though, the first pip is a much bigger deal than the other too. rF+ is very valuable. rF++ or rF+++ is almost never necessary outside of maybe orbs of fire.

The end result here is that AC is generally more important than resistances. If you're choosing between an armour with a much better AC, or one that gives you more resistances, chances are you want the one with more AC, unless you know you're going into a branch where that resistances is very important (e.g. Snake or Spider for poison, Cocytus for cold, Zot or Gehenna for Fire).

This is why, for example, crystal plate mail is generally considered better than gold dragon armour.

## What weapon should I use?

There are a lot of specific cases for this question, of course, but weapon selection comes up a ton so I thought I'd give some general guidelines.

The most important things to look at for a weapon are speed and base damage. A weapon's speed and base damage are much, much more important than its enchantment level, and usually more important than its brand. Quite often, the weapon you have with the best base damage per AUT is the best weapon you have, even if others have nicer enchantments or brands.

In the case of speed, a weapon's speed varies with your weapon skill. Specifically, every weapon has a base delay (the time it takes to swing the weapon with 0 skill) and a min delay (the fastest speed possible, usually 0.7). Every 2 weapon skill will lower the delay by 0.1. Generally, the bigger a weapon is, the slower its base delay, so the more skill it will require to hit min delay. This means smaller, faster weapons are sometimes better to use early on, but in the long term you'll usually want to use the highest damage weapon you can find, once you have the skill for it.

For a faster low-damage weapon vs. a slower high-damage weapon: Faster weapons benefit more from slaying bonuses and enchantment level (which add flat amounts of damage), and any brands that add flat amounts of damage (electric, chaos, distortion, pain). Slower weapons are better against enemies with high armour (which reduces damage by a flat amount) and with brands that boost damage by a % amount (flaming, freezing, vorpal).

### A quick guide to brands:

**Vorpal** (Slicing, Crushing, Chopping, etc): 16.67% bonus damage on average. Not the best brand, but always solid, since nothing resists it. A good general purpose brand on high-damage weapons, not as great on fast, low-damage ones.

**Flaming, Freezing**: 25% bonus damage on average of the corresponding element. Like vorpal, it's good for high-damage weapons, not as good for fast, low-damage ones. Tends to be better than vorpal, since it does more damage to more enemies, even if some can resist it. Freezing also slows cold-blooded enemies. Which one is better can vary by branch.

**Electrocution**: 1 in 3 chance of 8-21 damage. One of the best (and definitely the most general-purpose) brand you can get on fast weapon. A Quick Blade of Electrocution will tear things apart as long as they're not resistant to electricity. The damage is enough that it's a very good brand even on bigger, slower weapons, at least once they're at min-delay, although there it has to compete with flaming and freezing (not sure on exactly how the math works out there).

**Protection**: Most of the time, you want your weapon for damage, not defenses, so this is a weak brand. It can be handy early on, though, especially for casters who aren't counting on their weapon for damage and can often use the defensive boost.

**Venom**: A decent brand early on, when you can often kill dangerous enemies like ogres by stabbing them once or twice and then running away while the poison does its thing. Falls off heavily and is one of the worst brands later, though.

**Pain**: Flat damage based on your necromancy. Many enemies (including all demons and undead) are immune to it, but against anything that isn't immune, it's the best brand you can get if your necromancy skill is good. Pretty rare, but Kiku can gift it at max piety. Best on a fast weapon, but amazing on anything.

**Holy Wrath**: 75% bonus damage on average to demons and undead, nothing to anything else. One of the best brands possible (competing with anti-magic) for Pandemonium, the Hells, Tomb, and Crypt. Extremely situational and often just useless anywhere else. If you're going for 15 runes, you'll want one of these for the last 10. Otherwise, at best it's something you can switch to when a nasty demon or undead comes up, but that's it. The Shining one gifts this brand.

**Anti-Magic**: Gives enemy casters a chance to fail there spells (I don't know the exact mechanics), but reduces your max mana by 2/3. Trog gifts often have it. Not so great if your character is extremely mana-dependent and worthless against non-casters, but one of the best brands you can have against enemies that use spells if you can handle the mana penalty. It doesn't do any extra damage, but it's still worth it. Arguably better than holy brand for extended, since many of the biggest threats there are spells.

**Vampric**: A chance to heal when damaging enemies not immune to negative energy. Requires being full or above to equip, and makes you hungrier when you unequip it. It won't boost your damage and it's annoying to unequip, but against enemies not immune to it, this is one of the best brands you can have, the healing is amazing. If you find a high-damage vampiric weapon, consider it a keeper (at least for a 3-rune game, it becomes mostly worthless in extended).

**Chaos**: All sorts of weird effects, including flat damage, but also some bad ones like making enemies invisible or berserk. This can be a very powerful brand, especially on a fast weapon, but you're also liable to getting killed when it berserks the wrong enemy. Use with extreme caution.

**Distortion**: Flat damage, randomly blinks, teleports, or banishes enemies. Can do damage or even banish when unequipped, unless you worship Lugonu. Gifted by Lugonu. This brand can do amazing damage, especially on a fast weapon, the chance to banish enemies is lovely, and blinking or teleporting enemies away can be useful, but you can't really switch weapons unless you're worshipping Lugonu, and it can be a pain if you do most of your damage in melee and then blink a ranged enemy away. But it's very strong, if somewhat situational. Blink frogs are the only enemy in the game that resists its damage, as far as I know.

**Draining**: 12.5% + 1.5 damage on average, and applies a stacking debuff that's similar to lowering enemy HD (mostly lowers their spell damage and attack accuracy). Decent defensive brand, especially on fast weapons where you can stack up the buff quickly and beneft more from the flat damage, but it's nothing special and a lot of enemies resist it. Reworked in 0.15, if you see anyone talking about it reducing experience gain, that's outdated.

**Speed**: Makes a weapon 50% faster. Quite rare, and can only appear on some weapon types. Amazing on high-damage weapons like lajatangs or giant spiked clubs. Not as great on fast, low-damage weapons like short blades, since you'll attack crazy fast but do almost no damage to any enemy with moderate AC.

For **ranged weapons**, I'm not going to go into detail, but the main thing is this: flaming and freezing don't stack with your ammo's brand. Velocity and speed do, so they tend to be the best brands to get on your launcher. Speed is probably better, but rarer, so in most cases you'll want to find a velocity weapon.

## Weapon Types
This doesn't come up as often, but it does occasionally, so I thought I'd go over the weapon types.

**Short Blades**: Fast, low skill requirements, low damage, but great for stabbing. If you're a stabber, you want to use these for stabbing. Otherwise, you're usually better off with a higher damage weapon, unless maybe you're a small race (spriggan, kobold, or halfling), you find a really amazing short blade (probably electric, distortion, or pain), or you have ridiculously high slayng bonuses (not just on the weapon, but from other equipment too).

**Long Blades**: Long blades tend to have better base damage than other weapons, and moderate skill requirements. The best long blades (demon blade and bastard sword/double sword (depending on your version) for 1-handed, claymore/triple sword for 2-handed) are fairly rare, although a scimitar or great sword is still a very nice weapon. Triple swords/claymores are the highest base damage weapons in the game outside of Giant (spiked) clubs. In 0.15 and earlier, long blades that are blessed by The Shining One become blessed long blades with an extra base damage, but this is no longer true in trunk (Demon Blades still become Eudamon blades and get extra damage as a result, though).

**Maces and Flails**: Maces and flails tend to have lower skill requirements relative to their damage than other weapon types (besides staves). Morningstars are the best common one-handed weapon in the game, and great maces are the best common two-handed weapon in the game. Demon Whips and Eveningstars are also among the best one-handed weapons in the game overall. On the other hand, for most races, a great mace is the best two-handed mace they can use, and great maces don't do as much damage as the rarer two-handed weapons in most other categories. For a shield-user, maces and flails are one of the best weapon choices, since you'll almost certainly find a good morningstar some time in the early to mid game, and still have the potential to find an amazing eveningstar or demon whip. For two-handed weapon users, there's more of a tradeoff - you'll probably be smashing stuff with a great mace while someone using a different weapon type is using something weaker, but your maximum damage potential won't be as high. If you're an ogre or troll, things change, because you can get giant clubs and giant spiked clubs, the two highest base damage weapons in the game.

**Axes**: Axes tend to have very higher skill requirements and lower base damage than swords, but they cleave. In trunk, cleaving hits all adjacent units (including allies, so they're not ideal for anyone with a lot of allies around), in 0.15 it has some weird rules but the same basic idea. Because of this, axes are awesome when you're surrounded, but not as good as other weapon types in other situations. Ideally, you should avoid being surrounded at all, but sometimes it happens, especially if you're new to the game and not super skilled at positioning, and axes are great for making up for positioning mistakes if you can spare the experience. With some rare exceptions, one-handed axes tend to be terrible (broad axes, the best one-handed weapons, are as rare as the best one-handed weapons in other categories, but do much less damage), so you should almost always go 2-handed when using axes.

**Polearms**: Polearms have a similar skill requirement and damage to axes (i.e. good damage but not as good as long blades, very high skill requirement, especially for 2-handers). Instead of cleaving, however, they have reaching: when you're wielding a polearm, you can evoke it (v) to attack an enemy up to two squares away (unlike other ranged attacks, this can be two-squares in any direction, so you can target two diagonals away). This can be handy, although its use can be limited overall. They can still be a solid choice for some characters, especially merfolk (who have amazing aptitudes for them) and centaur (who can use their speed to kite enemies while poking them with reaching). Unlike axes, polearms do have a good one-handed option in demon tridents, although they're fairly rare and the next-best one-handed polearm, a regular trident, isn't as great. Spears are one of the worst weapons in the game, so if you start with a spear, try to replace it with a halberd, glaive, or trident as fast as possible (don't replace it with a scythe, which is possibly the single worst weapon base in the game, no matter what you may think when Sigmund kills you).

**Staves**: I'm gonna give enhancer staves their own category, since they're pretty different. There are only two types of normal staves: quarterstaves and Lajatangs. They are both great, however. Quarterstaves are generally considered the best starting weapon in the game, although only gladiators can start with them. Lajatangs are one of the most experience-efficient weapons in the game, requiring only 14 skill to hit min-delay while having a great base damage of 16 (for reference, great swords have the same base damage but hit min-delay at 18, and great maces and battle axes, with 17 and 15 base damage, respectively, hit min delay at 20). They don't do as much damage at min delay as the best two-handed weapons in other categories, but the experience you save getting them to min-delay can easily make up for it and make them awesome weapons. Lajatangs also come with the fairly rare speed brand, and lajatangs of speed are one of the best weapons you can find. So overall, staves are the most experience-efficient weapon type you can choose for any character not using a shield. The downside is that you can't start with a quarterstaff unless you're a gladiator, and there's no common option between quarterstaves and lajatangs (which can be moderately rare). Still, they're a solid choice, and any character who finds an early lajatang should strongly consider training staves if they're not to heavily committed to a different weapon type. They're especially nice for spell users seeking a melee option, since the low skill investment lets you save more experience for spells.

**Enhancer Staves**: Enhancer staves (staff of conjuration/summoning/fire/etc) give you a spell enhancer for a school of magic, giving a significant spellpower boost to all spells of that school. Their base type as a weapon is a plain staff, a base weapon so terrible plain ones were removed from the game. On the other hand, staves of fire, earth, ice, air, and death all do significant bonus damage based on your evocations and corresponding magic skill in the corresponding element (fire, physical, cold, electric, and negative energy, respectively). Necromany-users will often prefer a pain-braned weapon for their melee, but for anyone with significant training in fire, earth, ice or air magic, training evocations and using an enhancer staff is often the best choice for melee. Their damage is amazing, they hit min-delay at only 12 skill, they're one-handed, and they boost your spells. The main downside is that it's mostly useless against enemies immune to the damage type your staff does (unless you're using a staff of earth, since nothing is immune to physical damage).

**Further Adendum: I've been training weapon type X, but I just found a nice weapon of type Y. Should I switch?**

Usually not. A very good player once told me that he never even identifies any weapon that's not the base type he's training, no matter how good is has the potential to be.
There are some exceptions, of course. If you're not very committed to your current weapon type, the one you're switching to is really, really amazing, or you've got cross-training bonuses that will make the switch easier, then it can sometimes be worth it. But once I've got 10-15 or so skill in a weapon, I don't think I'd bother switching to any weapon type that I don't have cross-training in, and once I've got 20 I'd probably never switch at all unless I found the most mind-blowingly amazing weapon I'd ever seen (and even then, I'd need cross-training and still be hesitant). Overall, when in doubt, you probably shouldn't switch weapon types, and you definitely don't want to juggle your training around early in the game. It's usually best to just pick your weapon type and stick with it.

## Patashu's Tips

(8:50:09 AM) Patashu: Ok, I'll talk tactics (mostly melee positioning stuff) now

(8:51:07 AM) Patashu: 1) Rule 0: You should almost never move towards an enemy that is in your line of sight. It's not due to one reason, but it's a heuristic due to a few different reasons. In general, you usually want to retreat from an enemy you have just seen rather than approach it.

(8:52:47 AM) Patashu: 2) How noise works: Stuff like melee that isn't stabbing, most offensive spells, monsters shouting and you shouting creates a noise that radiates out in a circle and tries to alert monsters. Monsters alerted will be in a 'hasn't noticed you' state, but will be awake and will beeline towards the center of the noise, and then start wandering. If that brings you to their LoS, then they're only a stealth check away from starting to hunt you, but if it doesn't, they won't go looking for you because they don't know where to look, they'll just go back to random movement.

(8:53:29 AM) Patashu: So there's no such thing as 'pack coherence' in that you can get the attention of the first orc you see, beeline on a retreat path, and after 8+ tiles let it come to you and engage, and the other orcs will either have gone to the original noise and given up or not noticed at all depending

(8:55:06 AM) Patashu: This leads to the general framework for dealing with monsters that are or may be in dangerous groups: 'lure/split'. The moment you see a monster, stop moving towards it. If it hasn't noticed you yet, throw a stone/other ranged attack at it so it notices you (a trick called shoutless - if a monster is in wandering state and you hit it first, it never shouts, it always just silently goes to hunting state). Now back up 8-16 tiles towards a safe escape path (towards stairs, doesn't go through/towards unexplored territory), breaking LoS with corners/doors if you can. Let the one or two monsters come to you. Deal with them as an isolated, safe incident that you know won't attract anything else with the noise. Rest, repeat.

(8:55:57 AM) Patashu: If you don't do lure/split, and instead run at monsters on the edge of unexplored territory and fight them then and there (or even nearby), you'll feel like every battle is an endless torrent of enemies and huge groups streaming in, because the noise of the battle 1) attracts enemies in the unexplored territory 2) they see you 3) they join in the battle guaranteed

(8:56:42 AM) Patashu: Doing lure/split also means you can use things like berserk/all your MP in more comfort and safety, because you are almost guaranteed that no other enemies will show up after the battle ends

(8:58:48 AM) Patashu: 3) Doors are OP

(8:59:59 AM) Patashu: 3a) A surprising number of monsters can't do anything about doors. Anything that has hands can open them, but basically any animal or monster can't, even things like drakes, dragons and elephants that you wouldn't expect to be stopped by a door (the unique Xtahua is a notable exception, being a dragon that can open doors - however, the unique Prince Ribbit, a blink frog, cannot)

(9:00:39 AM) Patashu: 3b) If the monster is the same speed as you, you can close the door as fast as it can open it. This leads to a technique called 'door dancing', where as long as you and the monster are the only thing around the door, you can repeatedly close the door to recover HP/MP/stall for time otherwise.

(9:00:55 AM) Patashu: 3c) If you just opened a door and see a bunch of shit you don't want to deal with, the first step is usually closing the door to break LoS

(9:02:21 AM) Patashu: 3d) If your stealth is meaningful, breaking LoS with an enemy is a requirement for it to forget about you/stop hunting about you, so if you close doors on enemies with good stealth some of them will stop hunting you as you keep doing this, and since it takes them just as long to open it as you did to close it, it's not 'losing turns'

(9:03:52 AM) Patashu: 4) Energy randomization. In Crawl, for monster movement only, there is a random chance that the monster movement will happen 10% faster or slower. These 10% fasters and slowers add up, and eventually the monster will fall behind a tile or advance an extra tile. (If you see one happen, the other is likely to happen again soon, due to the energy randomization going in the opposite direction.) This also applies for opening/closing doors, but it doesn't apply for the monster attacking or casting. If a monster suddenly gains or loses ground on you, this is probably why.

(9:04:55 AM) Patashu: This is what makes the smallest case of 'pillar dancing', where the pillar is only one tile wide, not work reliably (but larger pillars are usually fine depending on the monster), and it is also why 'door dancing' will eventually fail with the monster stepping into the door after opening it on the same turn

(9:08:43 AM) Patashu: 5) Corners are OP. Going around a corner, like a door, is one of many ways to 'break LOS' (there is also fog/smoke/steam, allies/summons, blinking/teleporting away, wielding a lantern of shadows, etc). A monster with broken LOS has to come up to one tile away from you (if it's a tight 90 degree turn) or even next to you (if it's a tight 180 degree turn) before it can fight you again, and this lets you maximize the amount of time you are meleeing them from if you want to kill them, or maximize the amount of time they can't see and thus shoot at you if you want to run away from them.

(9:09:46 AM) Patashu: (also, don't forget about lure/split - you might want to not stop at the first corner/door, but back up 8+ tiles to a corner/door closer to the stairs, so you're not just breaking LoS BUT splitting the group at the same time)

(9:12:21 AM) Patashu: 6) Weapon swap trick. This only works on monsters that have a slower-than-you-can-take-a-step melee attack, due to having a very heavy melee weapon in their hands (ogres and their clubs are the most common reason). Here's how it works: After said monster swings, it takes more than 1.0 of a turn before it can take its next move. With the monster next to you, swap weapons or take off/put on one piece of jewellery (both are the fastest action you can do with any character) until the monster swings. Step away. A gap will almost always form. Why would you want a gap? A few good reasons are 1) You want to take the stairs (if the monster is not next to you when you START taking the stairs it cannot follow) 2) You want to cast conjure flame or otherwise make a summon in the tile between you both that requires an open tile

(9:14:56 AM) Patashu: Btw, a monster with a weapon in its hands is a lot more dangerous than one without, instead of doing 1d(hands damage) then subtracting 1d(your AC) it does 1d(hands damage + base damage of weapon) then subtracts 1d(your AC)

(9:15:02 AM) Patashu: (Base damage of the weapon being what it says when you examine it)

(9:15:27 AM) Patashu: And brands work for enemies the same way they work for hands, so a monster with a glowing/runed/shiny weapon might be packing electrocution or distortion

(9:20:43 AM) Patashu: 7) Monster blocking tricks. There are a few ways you can get monsters to unhelpfully block other monsters:
7a) If you're standing next to a sufficiently 'respected' monster that is not hellfire resistant, enemies won't cast hellfire at you (because it is area of effect) (in particular, deep elf sorcerers are not themselves hellfire resistant, so they will never hellfire you in melee, except maybe to suicide?) (there are some other kinds of area of effect attacks that this will work with, but hellfire is the most notable example because it's really dangerous)
7b) Monsters that are approaching you tend to funnel towards the orthogonals ('enemy funneling rule'), so if there is an enemy on that orthogonal, enemies behind it will lose LoF and not be able to cast LoF requiring spells at you (you can also do this on a diagonal, but it's really stupid to visualise if it will work or not, so it becomes probabilistic trick if you don't have a lot of enemies on that diagonal for blocking)
7c) Stronger monsters will push past weaker monsters to get into combat with you... BUT, if the monster is confused/paralyzed/petrified/constricted/netted/batty (bat, harpy, unseen horror, etc) then the monster cannot be pushed past!

(9:26:08 AM) Patashu: 8) Folly of friendship trick. Monsters that are animal intelligence or higher, if they see another monster behind them that would like to join the melee but is chokepointed and can't reach you, they will step to another tile adjacent to you so that that monster can also attack you. So imagine there's two orcs next to the 'elbow' of a corner and you're fighting the first one on the diagonal. Eventually it will decide to step into the elbow of the corner instead of attacking back so its friend can step in. Now take a step back. You have essentially gotten a free hit without retaliation when this happened. Doesn't sound like much - until you realize that if you have a large loop of sharp corners to pillar dance the orcs through, you can do folly of friendship trick over and over.

(9:27:03 AM) Patashu: (The corollary of folly of friendship trick is that you should never stand in the sharp elbow of a corner while fighting a group of enemies, because eventually the front enemy will move to trap you into that elbow - but being in the sharp elbow of a corner is bad for other reasons too, it's usually a wasted move that would be better spent cutting the corner with a diagonal so you are moving/escaping/breaking LoS faster)

(9:28:54 AM) Patashu: This is a minor trick relative to the previous 7

(9:34:01 AM) Patashu: 9) Hack and back. This tactic requires you to attack (thus know your weapon delay) faster than the enemy moves, so it usually only applies to zombified/skeletal enemies, elephant slugs, goliath beetles and early game worms. If you wait near a slooow monster until it steps next to you, hit it with your sufficiently low delay weapon and then walk away and repeat, it will never hit you once. (EDIT: In 0.15 most slower-than-you melee-only monsters are being removed, but you can still create hack and back situation with haste or by slowing the enemy.)

(9:29:48 AM) Patashu: Ok, now let's talk about skilling

(9:30:21 AM) Patashu: 1) Here is how you skill in Crawl. You raise your killdudes skill until your killdudes options are online. Then you train the skills that help you not die to dudes. If in the future you're having trouble killing dudes again, swap back to killdudes skills.

(9:31:42 AM) Patashu: 2) Melee weapons have a concept called 'min delay'. Examine the weapon and look at what its delay is - every 2 skill for that weapon, it will drop by 0.1, until it reaches 0.7 (if it is 1.4 or heavier) or half the original rounded down (if it is 1.3 or lighter, e.g. a 1.0 weapon reaches 0.5 after 10 skill, and a 2.0 weapon reaches 0.7 after 26 skill)

(9:32:15 AM) Patashu: The closer you are to getting a weapon to min delay, the more rapidly training it and using it gets better - until you reach min delay, after which the benefits of further training that weapon skill are a lot more marginal, so unless you can find a heavier weapon to swap to, you should train notdietodudesskills now

(9:32:52 AM) Patashu: (Also, the advantage of a heavy weapon's higher base damage isn't just a constant addition of damage - the base damage is multiplied by your skills, whereas enchantment and slaying damage is just added on unmultiplied, so heavier weapons will hit a lot harder than the numbers indicate, if you can get them to respectable minimum delay

(9:35:33 AM) Patashu: Also, random comment, the skill 'evocations' improves elemental evokables (that go in the misc category of your inventory), rods and wands by a LOT, but ofc if you're training evocations that's exp not going anywhere else, for something that can run out, so it's an opportunity cost thing, but a bit of evo makes wands a lot better

(9:39:27 AM) Patashu: Also, how to handle the Identification Minigame in Crawl:
1) Read all unidentified scrolls when you're not in danger to ID (the floor is 100% cleared - otherwise teleportation could put you in the middle of angry monsters)
2) Use identify scrolls ASAP on unidentified potions in your inventory, don't quaff potions to find out what they are unless it's literally the only way to not die left
3) Once you have most/all of the potions out of the way, you can start using identify scrolls on other stuff
4) AS LONG AS you have one or more remove curse scrolls available, don't use identify on weapons/armour/jewellery to identify them, put them on first to get a wear-identification. (The only thing you need to worry about are weapons of distortion, so don't wield random junk ego weapons unless you'd be happy with being stuck with them as distortion until xl18 or so)
5) Zap unidentified wands the moment you see them, if you're playing 0.14 or later you don't need a target, they identify automagically.

I also think that your first win should be Minotaur or Gargoyle Berserker, because they and their god's abilities are tuned for melee fighting and it forces you to make use of all melee tactics and positioning techniques, while at the same time not having to worry very hard about skilling or building your character (just always pick dex for the stat, always wear the heaviest armour you can find and the biggest weapon that you've trained to mindelay, train weapons until mindelay then swap to fighting/armour and later dodging, maybe evo if you find good evokables, that's basically it already!). You can of course do your first win with anything, but then you are learning two things at once, both how to play Crawl and how this specific start needs to be built and played to survive well.

(9:56:41 AM) Patashu: Also, in Crawl your HP melts very fast and restores very slow

(9:57:02 AM) Patashu: If a fight could potentially go south, at 100% hp you should already be acting cautiously/safely, making sure you have a good retreat line to the stairs, thinking about what you'll do if it starts to get hairy, etc

(9:57:15 AM) Patashu: At 75% hp you should already be ready to use consumables/abilities/powers or think about retreating

(9:57:32 AM) Patashu: At 50% hp your life is in danger and you should treat the situation like it could kill you right now

(9:57:57 AM) Patashu: Don't let it drop any lower because then you don't have any 'buffer' left at all, a lucky hit can do 20~ and later in the game 50++ damage

### Bot Commands
command                     | result
-------                     | ------
??                          | query the crawldb
@??                         | get monster stats
!hs * vp en god=ash -4 -log | useful for finding successful builds with X god etc
!help                       | a list of most of the bot commands

### Links

 * [cbro webtiles](http://crawl.berotato.org:8080)
 * [Play DCSS Online](http://crawl.develz.org/wordpress/howto)
 * [tournaments](http://crawl.develz.org/wordpress/category/tournament)
 * [OCTOLOG](http://octotrog.berotato.org/)
 * [dump of bang commands used in #octolog](bang_commands_dump.txt)
 * **Resources**
    - [Search LearnDB](https://lookupdb.guy.ht/)
    - [LearnDB](https://loom.shalott.org/learndb.html)
    - [Crawl Wiki](http://crawl.chaosforge.org/Crawl_Wiki)
    - [!lg manual](https://github.com/crawl/sequell/blob/master/docs/listgame.md)
    - [RC Options](http://git.develz.org/?p=crawl.git;a=blob;f=crawl-ref/docs/options_guide.txt)
    - [cbro rcfiles](http://crawl.berotato.org/crawl/rcfiles/)
    - [MarvinPA rc](http://crawl.develz.org/configs/trunk/MarvinPA.rc)
 * **Communities**
    - [/r/dcss](http://www.reddit.com/r/dcss)
    - [The Tavern](https://crawl.develz.org/tavern/)
 * **Dev**
    - https://gitorious.org/crawl (also: [Cheibriados' cloned repo](http://s-z.org/neil/git/?p=crawl.git;a=summary))
    - [Bug Tracker](https://crawl.develz.org/mantis/main_page.php)
    - [Mailing List](https://lists.sourceforge.net/lists/listinfo/crawl-ref-discuss)
 * http://www.reddit.com/r/dcss/comments/1hetzj/how_to_not_grind_interface_usage_dont_do_work/
 * http://www.reddit.com/r/dcss/comments/2mjo74/frequently_asked_questions_common_misconceptions/

