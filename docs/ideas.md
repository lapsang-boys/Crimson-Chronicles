
# TD documentation

## Terminology

__Zones:__
A collection of levels.

__Area:__
A player area in a _zone_ where the player builds towers to defend against waves
of mobs.

__Alexandria:__
The system which enables us to retrieve class information about
mobs and towers.

## Gotchas

### Mobs

Here are some important (and unintuitive) fields in the object definitions of
mobs:

__Point value.__
This represents the bounty the player receives if the mob leaks.

__Food used.__
This represents the number of lives that are taken from the player when the mob
leaks.

__Notes when creating a new mob:__

When creating a new mob type, you'll have to write a new class that overrides
the respective method in `MobWrapper`.

* onEnter
* onDeath
* onTick

You'll also need to write a Hooker so that the spawn system can add the unit to
Alexandria.

### Towers

Here are some important (and unintuitive) fields in the object definitions of
towers:

__Point value.__
This represents the gold the player receives when the tower is sold, including
previous gold costs spent for upgrades. Example: `Tower A` costs 10 gold and
upgrades to `tower B` for 15 gold, then the point value for `tower A` is 10 and the
point value for `tower B` is 25.

__Notes when creating a new tower:__

If the tower will utilize towers or create units/items/etc. it should be
placed into _Alexandria_ in `TowerHook.wurst`.

## New Mechanics

### Disenchant / Dispel

Enable some towers to prevent some units from triggering their mechanics. For
example prevent benders teleports, unsummon etc. It's worth discussing for
making the TD more tactical.

## Zones

### Felwood / Protection of Ashenvale

__Boss:__

Ancients of Withergrove

_Description:_

A group of corrupted ancients in a squad. Use the purple corrupted ancients model files.

Tree of life is enveloped in a defense spell which makes his armor really high.
Killing the Ancient of Lore removes the protection from the tree of life.
Killing the Ancient of Wind reduces the squads movement speed.
Killing the 

Ancient Protector
Ancient of War
Ancient of Wind
Ancient of Lore
Tree of Life
Tree of Ages
Tree of Eternity

_Mechanics:_

???

__Terrain:__

Forest / Fel corruption

Transitions from Felwood to Ashenvale, maybe use green immolation fire for fel
corruption effects in terrain.

__Fauna:__

Demonic satyrs / Infernals /
Rotting treants and ancients /
Corrupted Furbolgs / Oozes /
Felbeasts

##### Mob ideas

* _Level 1:_ Stag
* _Level 2:_ Felbeast
* _Level 3:_ Demonic Satyrs
* _Level 4:_ Fel Treants
* _Level 5:_ Dark troll pack
* _Level 6:_ Oozes
* _Level 7:_ Demonic Satyr platoon
* _Level 8:_ Corrupted Furbolgs
* _Level 9:_ Druid of the Talon
* _Level 10:_ Boss (Ancients of Withergrove)

---

__Stag__
Plain.

__Felbeast / Dire Wolf__
MobType.AGILE

__Demonic satyrs__
MobType.DEMON

__Fel Treants__
When the fel treants die they will pollute the nearby towers effectively
making them stunned for a short duration.

__Dark troll pack__
Faith and war stomp heal

__Oozes__
Starts with lots of small oozes and then the collect and merge into larger oozes
at the first node. Maybe MobType.BANISHED

__Demonic Satyrs Platoon__ 
Spirit linked with each other so injuring one of them divides the damage to the
other. Fast runners and meaty tanks combination.

Invisible, MobType.DEMON, Evasion

__Corrupted Furbolgs__
MobType Taunt, slow meaty mangaz, 
Healer, healing wave, rejuvenation
MobType.BENDER, speedy
Entangling roots animation, or earth bender animation.

__Fallen Druids__
When the druids only have 30% of their HP left they will transform into ravens.

---

### Stratholme / The Culling of Stratholme

__Boss:__

The Four Horsemen

_Description:_

Four death knights on deathchargers. Think undead Arthas hero.

https://www.hiveworkshop.com/threads/baron-rivendare.301727/
https://www.hiveworkshop.com/threads/deathknight.211062/

_Mechanics:_

Can only die together

Death coil

???

__Terrain:__
City / Burning / Destroyed / Eastern Plaguelands

__Fauna:__
Abominations / Crypt fiends /
Banshees, Wraith, Shades /
Dreadlord - Balnazzar /
Gargoyles / Ghouls, Zombies /
Skeletals / Necromancers

#### Mob ideas

__Plague rats__
Lots of plague infected rats tries to escape the inferno of Stratholme. Creates
a cloud of poison gas when killed, damaging nearby rats. Maybe also
MobType.AGILE

__Abomination__
The level begins with lots of friendly humans trying to escape quite slowly
through the players maze. Then one abomination will be released which gets
increased movement speed or health every time it reaches a human and devours it.
Alternatively it can use the meat hook and play fresh meat sound when eating a
villager.

__Banshees, Wraiths, Shades__
A squad with quick spawn interval, low hp, evasion and periodic invisibility.
Their weak point is their low hp.

__Cult of the Damned / Necromancers__
When reaching a node they summon skeletons. When skeletons are killed they
injure their summoner. The necromancers have high magical armor so it's worth
focusing on the skeletons to deal serious damage.

__Gargoyles__
Flying units that will go into stone form when only 30% of their life remain.
Where they gain increased life regeneration for 5 seconds and then resume their
escape. This can only happen once and will not loop.

__Deceived Crusaders__
Crusaders tricked from their mission against the Scarlet Crusade by Balnazzar to
protect the last humans of Stratholme. Spawns with many infected humans who will
turn to Ghouls and Zombies when reaching nodes.

__Meat Wagon__
When a meat wagon reaches a node they will catapult a ghoul towards the next
node. Carriying infected corpses and ghouls. When a meat wagon is destroyed,
the remaining ghouls and zombies will awaken to continue their onslaught.

__???__


__Dreadlord__
Creates many illusions which will move in synchronization with the dreadlord, but are
slightly transparent and color shifted with no pathing. The user should focus
fire on the real dreadlord. The ability will look like a mirage.

Other spells in his wc3 repertoire: Sleep, Drain Life, Rain of Chaos and
Earthquake.

---

__Liches__
Balzaphone

https://wow.gamepedia.com/Balzaphon

__Frost wyrms__

* _Level 1:_ Plague rats
* _Level 2:_ Abomination
* _Level 3:_ Banshees, Wraiths, Shades
* _Level 4:_ Necromancers
* _Level 5:_ Gargoyles
* _Level 6:_ Deceived Crusaders
* _Level 7:_ Meat Wagons
* _Level 8:_ ???
* _Level 9:_ Dreadlord - Balnazzar
* _Level 10:_ Boss (The four horsemen)

### Caverns of time

__Boss:__

Twins of time

_Description:_

???

https://www.hiveworkshop.com/threads/icecrown-seer.294497/
https://www.hiveworkshop.com/threads/inquisitormalendis.200540/
https://www.hiveworkshop.com/threads/diablo-iii-king-leoric.224358/

_Mechanics:_

The twins will take turns in casting time shift, has permanent slow aura and
haste aura.

Time shift works by channeling for a few seconds and then a circle will be
placed at the casters feet. Then after 10 seconds, the caster will be returned
to the circles position and it's hp will be returned to what it was when the
circle was created.

The twins has one unique aura each. One has a slow aura for the players tower
and the other twin has a haste aura for the movement speed of the twins. When
one twin is time shifting, the other one's aura is activated.

__Terrain:__
Barrens / Sand / Desert / Cliffs

In a rocky desert train with stormy weather, you'll defend the realm against
waves of historical monsters unleashed from the caverns of time.

__Fauna:__
Old races / Squads

_Nerubians_

https://www.hiveworkshop.com/threads/crypt-warlock.197086/
https://www.hiveworkshop.com/threads/spider-warlord.124562/

#### Mob ideas

__Faceless ones__

__Kobolds__

__Dragons__
Flying whelps, dragons and wyrms with dragonspawn on the ground.

__Nerubians__
Lead by Anub'arak. When reaching each node, nerubians will unborrow from
underground to ambush your maze. Lesser spiders as well.

__Gurubashi__
Ancient troll empire. Collection of various trolls.

__Goblin Explorers__
A goblin caravan. Consists of goblin demolitioners, goblin zeppelins, goblin
woodcutters, and maybe more goblin imports from hive.

__Fel Orcs__
Grom Hellscream, and other corrupted orcs.

__Burning Legion__
Kel Thuzad, Pit lord, felguards, succubi, doom guard, etc.

__Eredar warlocks__

* _Level 1:_ ???
* _Level 2:_ ???
* _Level 3:_ ???
* _Level 4:_ ???
* _Level 5:_ ???
* _Level 6:_ ???
* _Level 7:_ ???
* _Level 8:_ ???
* _Level 9:_ ???
* _Level 10:_ Boss (Twins of Time)

### Misc mob ideas

__Hydra__
One large hydra which will spawn 3 lesser hydras when destroyed, and
the same thing applies to those hydras.

__Infernals__
One large infernal, summons lesser infernals when reaching each
node.

__Dragonspawn__
Single dragonspawn walking and periodically dropping eggs that
hatch after a while.

__Hippogryphs__
Agile and meaty flying beasts, can possibly be combined with archers that are
dropped to be a combined level. Slight conflict with lore if we use nightelf
archers though, but can be fixed with a lil' tweak in vertex color ;)

__Chimeras__
Massive flying beasts, when reaching a node they summon tornadoes when moving
around causing mobs to become temporarily stunned when hit by the tornado and
miss when being close to the tornado.
