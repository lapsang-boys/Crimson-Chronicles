<p align="center">
  <img src="https://i.imgur.com/v08jhrY.jpg">
</p>

_Desperate times calls for desperate measures. Our hope lies in the brilliance of inexperienced tacticians leading the vanguard against the looming threats in the horizon._

_In Ashenvale the Sentinels are drawing their last breath; Felwood spreads its corruption in an unending invasion. Mysterious and mutated beasts alongside devilish Satyrs welcome the Sentinels call for aid with renewed bloodlust. Fight back the corruption and protect the Sentinels outpost at all costs!_

_Meanwhile, the Scarlet Crusade rallies all able-bodied men and women to aid them in a final assault on the Lost city. The summons traveling by word of mouth instill a sense of urgency: "The moment has finally come to purge Stratholme once and for all! With the light radiating on our backs we will charge the horrors of The Scourge. Join us and together we shall end this nightmare that has haunted us for far too long!"_

_In the midst of these calamities, the drums of war thunders over the desert plains of Tanaris like a rolling storm. Long gone empires will wave their banners for supremacy once again when the Caverns of Time soon opens its portals. Only the most versatile tacticians will stand a chance against the genius warlords from the distant pasts._

<p align="center">
  <i>Countless lives will be lost, but the canvas of war will never paint a more beautiful view. The red ink will fill the pages of the Crimson Chronicles.</i>
</p>

# Crimson Chronicles [TD]

Welcome to the project page of Crimson Chronicles (CCTD for short), a tower defense set in the Warcraft lore. It will feature a polished game experience with many new mechanics for tower defense connoisseurs to enjoy, for instance we boast of (soon to be) three separate zones in different biomes and layouts with increasing difficulty and tactical elements.

Crimson Chronicles [TD] in a few keywords: mazing, node-based, 100% sell, polish, unique mobs, hard, innovative and fun.

This map has been in the development for many years now, where the first iteration of the map started around 2007. The names have varied throughout the years (in chronological order): Pirate TD, Trocadero TD, Defense of the Deserted, Dictator's Execution and finally Crimson Chronicles which is actually the first map we've ever published.

## Development

In order to build the map you'll need the wurst compiler installed and VSCode, install instructions can be found in the `Wurst` subsection.

### Wurst

Install instructions for Wurst: https://wurstlang.org/start.html

### Update Object definitions

Crimson Chronicles uses a spredsheet for balancing our towers which needs to be merged into the wurst project, for that we created the tool [Exicon](https://github.com/lapsang-boys/exicon.git).

```shell
$ cd crimson-chronicles
$ git clone git@github.com:lapsang-boys/exicon.git
$ python exicon/update.py
```

## Authors

Karlek & Godbit
