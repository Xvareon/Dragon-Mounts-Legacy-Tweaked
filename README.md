# Dragon Mounts: Legacy Tweaked

MOD LINK: [Dragon Mounts Legacy Tweaked](https://www.curseforge.com/minecraft/mc-mods/dragon-mounts-legacy-tweaked)

> **NOTICE:** This is a fork of Dragon Mounts: Legacy by Kay9Unit. For the original mod please go to their page. All credits go to them and their contributors, but **do not report bugs caused by this fork to them!** Report it to me instead.

This mod is incompatible with *Dragon Mounts Patches* since it incorporated the issues that *Dragon Mounts Patches* fixes. The mixins will be incompatible with the base code. This is also incompatible with the original *Dragon Mounts Legacy* mod as this is a standalone mod, be advised.

---

## TWEAKS

* **New Dragon Breaths!** Besides Fire, there are Ice, Storm, Wither, Sculk, and Ender Breaths now corresponding to appropriate dragon breeds.
* **Combat AI:** Dragons now shoot breath balls when in combat. They still use melee when in close range.
* **Keybind Attack:** When ridden, dragons can shoot fireballs via keybind (default: `G`).
* **Dual Riding:** Dragons can be dual ridden by players.
    * The owner is the only one that can control the dragon.
    * The owner is the only one that can activate the fireball breath via keybind.
    * When the owner dismounts, dies, or disconnects, the 2nd passenger will be forcefully dismounted as well.
* **Armor Mechanics:** Dragons can now be given armor via Copper, Iron, Gold, Emerald, Diamond, and Netherite blocks. Each provides a different armor value. Armor can be retrieved via shears like the saddle. If given another block while wearing armor, the armor will swap and the player will get the previous armor's block back.
* **Chest Mechanics:** Players can give dragons a chest and access them via keybind (default: `H`) whenever they are riding them or looking at them (vanilla interaction range). Chests can be retrieved via shears like the saddle. If the dragon dies or the chest is sheared away from the dragon, the contents drop to the ground.
* **Wander Mode:** In this state, the dragon will be anchored in an area. The area size is configurable. To set your dragon to wander mode, simply Shift + Right-Click (like how you make them sit or follow). There will be text indicating which mode they are currently in (this also shows when dismounting). The modes cycle through three states: **sit**, **follow**, and **wander**.
    * When you ride the dragon upon setting them to follow or wander, they will retain that mode upon dismounting.
    * However, when the dragon is in sit mode and you ride and dismount, they will be in a 4th mode (neutral mode, they don't go back to sitting).
* **New Dragon Textures and Dragon Types!**
* Updated the textures of some of the original dragons.

### Additional Adjustments

* **Healing:** Vanilla and Modded fish items can now heal dragons which previously cannot.
* **Aether Dragons:** Can now be hatched via glowstone blocks.
* **Hotfeet Ability:** Can now turn wet sponges into sponges and blackstone into magma blocks (inverse of *Hydrostep*).
* **Dragon Variant Attribute Tweaks:**
    * All dragons are fire immune.
    * All dragons have increased health and armor.
    * All dragons have natural regeneration.
    * End Dragons and Water Dragons have increased HP.
    * Ice Dragons and Fire Dragons have increased damage.
    * Forest Dragons have increased movement speed.
    * Aether Dragons are unchanged (their `+flight speed` attribute is sufficient).
    * Nether Dragons are unchanged (their default `+armor` is sufficient).
    * Ghost Dragons have less HP, but gain armor toughness and arrow immunity.

### New Dragon Breaths & Breeds

* **Storm Dragon:** Lower armor with slightly fast movement speed, flight speed, melee damage, and is immune to lightning bolt damage. Can be hatched when surrounded by copper blocks. It has the *Electro Step* ability that cleans weathered copper.
* **Blue Fire Dragon:** Can be hatched via obsidian. It breathes blue fire (cosmetic change from normal fire breath).
* **Terra Dragon:** Increased HP and armor, immune to stalagmites and stalactites. Can be hatched via andesite, granite, diorite, and terracotta blocks.
* **Zombie Dragon:** Less armor and HP, but immune to drowning, suffocation, poison, and magic. Can be hatched via bone blocks. Has the *Putrid Step* ability which occasionally:
    * Turns grass blocks into Moss, Mycelium, or Coarse Dirt.
    * Places dead bushes in sandy terrain.
    * Places mushrooms.
* **Solar Dragon:** Immune to withering. Can be hatched via gold blocks.
* **Lunar Dragon:** Immune to withering. Can be hatched via crying obsidian.
* **Aurora Dragon:** Immune to freezing. Can be hatched via purpur blocks.
* **Magic Dragon:** Immune to magic. Shoots ender breath balls. Can be hatched via enchantment table blocks.
* **Crystal Dragon:** Increased HP and armor, immune to stalagmites and stalactites. Can be hatched via amethyst blocks.
* **Bronze Dragon:** Same attributes as Storm Dragons. Can be hatched via redstone lamps.
* **Soul Nether Dragon:** Soul Fire-able blocks can no longer hatch the Nether Dragon; it will instead hatch this new variant (cosmetic change only). Can be hatched by blocks that emit soul fire.
* **Ocean Dragon:** Prismarine and Sea Lanterns can no longer hatch the Water Dragon; it will instead hatch this new variant (cosmetic change only).
* **Wither Dragon:** Immune to withering, slightly low HP. Shoots wither skulls which inflict withering. Can be hatched via wither skeleton skulls. Has the *Wither Step* ability that occasionally spawns wither roses and soul soil on blocks it walks on.
* **Gale Dragon:** Very similar to Aether Dragons. Can be hatched via blue terracotta blocks.
* **Sculk Dragon:** Immune to in-wall damage and sonic booms. Can be hatched via sculk blocks. Shoots Sonic Boom breaths. Has the *Sculk Step* ability which spreads sculk.
* **Primal End Dragon:** Can be hatched via endstone.
* **Primal Nether Dragon:** Can be hatched via red terracotta blocks.
* **Eclipse Dragon:** Can be hatched via yellow terracotta blocks.
* **Dark Dragon:** Can be hatched via black terracotta blocks. Shoots wither breath balls. Immune to lightning bolts and freezing.
* **Black Fire Dragon:** Can be hatched via black concrete. It breathes black fire (cosmetic change from normal fire breath).
* **Sylphid Dragon:** Immune to drowning, slightly faster flight speed. Can be hatched via light blue terracotta.
* **Monarch Dragon:** Increased HP, armor, and damage, but susceptible to Minecraft's dragon breath damage. Can be hatched via red glazed terracotta.
* **Jade Dragon:** High armor and armor toughness, reduced HP, slightly faster movement speed. Can be hatched via emerald blocks. Has the *Jade Step* ability that occasionally turns stone or deepslate into emerald ore.
* **Red Dragon:** Slightly higher HP. Can be hatched via red concrete.
* **Elder Dragon:** Similar to the Monarch Dragon, but breathes blue fire. Can be hatched via gray terracotta.
* **Shadow Dragon:** Similar to the Monarch Dragon, but breathes black fire. Can be hatched via black glazed terracotta.
* **Light Dragon:** Shoots storm breath balls. Immune to lightning bolts and freezing. Can be hatched via white terracotta.
* **Blood Dragon:** Similar to the Monarch Dragon. Can be hatched via redstone.

### Dragon Breath Mechanics

* **Fire Breath:** Sets entities on fire when directly hit if they are not fire immune and are within the explosion radius.
    * Ensures consistent damage and fire application.
    * Respects `doFireTick` and `mobGriefing` gamerules.
    * Lights up lit blocks such as candles, campfires, redstone lamps, smokers, furnaces, blast furnaces, and TNT. Modded blocks with the `LIT` blockstate will also be lit.
    * If the block has the `SOUL_FIRE_BASE_BLOCKS` Minecraft tag, it will set it to soul fire instead.
    * Expires immediately upon touching water and cannot pass through water (except for Black Fire breath).
* **Ice Breath:** Applies the freeze effect to mobs not immune to freezing. Has a chance to summon a snowfield upon impact/explosion that slows and applies Mining Fatigue to mobs. Extinguishes surface fires and unlights blocks (campfires, candles, lamps, etc.). Turns water into ice and lava into cobblestone/obsidian.
* **End Breath:** Has a chance of summoning a harming cloud upon impact/explosion.
* **Storm Breath:** Has a chance of summoning lightning upon impact/explosion and a lightning field that stuns contacting mobs. Emits redstone signals when hitting lightning rods and cleans copper. Can transform mobs (e.g., creepers into charged creepers, pigs into zombie piglins).
* **Wither Breath:** Inflicts withering on entities in the radius and places wither roses on victims. Respects Minecraft griefing rules.
* **Sculk Breath:** Inflicts darkness and knockback over a larger radius compared to other breaths. Triggers a sound event to activate sculk sensors.

### Miscellaneous Improvements

* Updated JP and UK translations.
* Added Chinese, Russian, Spanish, French, and Portuguese (South American and European) translations.
* Tweaked dragon tails of Nether, Water, Ghost, and Forest dragons.
* Added configurations for dragon breaths.

---

> Huge thanks to the **Dragon Mounts 2** team for allowing me to use the updated textures for dragons!
>
> * **Dragon Mounts Discord:** [https://discord.gg/Ewm8aTTJ3K](https://discord.gg/Ewm8aTTJ3K)
> * **Dragon Mounts 2 (1.12.2):** Check out [Dragon Mounts 2 on CurseForge](https://www.curseforge.com/minecraft/mc-mods/dragon-mounts-2)!

---

## FAQ

#### Q: How do I get dragons / dragon eggs?
**A:** There are two ways:
* **Option 1:** Kill the Ender Dragon again by respawning it, then transform the egg into your preferred variant. (In the config, the dragon egg will always spawn at the dragon fountain unless a mod conflicts).
* **Option 2:** Find them in chests like the original mod (disabled by default). Enable `use_loot_tables = true` in the configs and restart the game. New egg variants share spawn weights with base dragons (e.g., increasing Aether Dragon spawn weight also increases Gale Dragon spawn weight).
* See the [Global Loot Modifiers Reference](https://github.com/Xvareon/Dragon-Mounts-Legacy-Tweaked/blob/mc/1.20-updates/src/generated/resources/data/forge/loot_modifiers/global_loot_modifiers.json) for details.

#### Q: I can't open my dragon's inventory. Why is this happening?
**A:** Your keybind might conflict with another mod. Change the dragon inventory keybind in controls to resolve this.

#### Q: My game is crashing. What could be the problem?
**A:** You may be running *Dragon Mounts Patches*, which is incompatible with this mod from version 9983 onwards (its fixes are already integrated). If that is not the cause, attach your crash log via text file in the comments or GitHub issues page. **Without a crash log, troubleshooting is not possible.**

#### Q: Is this compatible with DML's addons?
**A:** Probably not. You can test it though. Some bugs might occur.

#### Q: I am creating a custom breed via datapack and want to set its breath type. How do I do that?
**A:** Include the breath string in your breed's name. For example, a breed named `"mutant_sculk"` will automatically use sculk breath.
* **Available breath strings:** `fire` (default), `ice`, `storm`, `wither`, `end`, `sculk`, `blue_fire`, `black_fire` (e.g., `"x_ice"`, `"ice_x"`).
* You can edit language files to display a clean name in-game while maintaining string detection.

#### Q: Why are my egg textures bugged/missing?
**A:** You likely have a certain version of Embeddium and Modernfix. Simply update those two and this will be fixed.

#### Q: I switched from base Dragon Mounts Legacy to this mod and attributes (HP, flight speed, armor) are not updating correctly. Why?
**A:** Previous versions preserve entity attributes in existing worlds. New attribute values apply only to newly hatched dragons or updated versions. It is recommended to update to the latest version and hatch new dragons (existing dragons will remain as "Legacy" dragons).

---

> **WARNING:** DO NOT DOWNLOAD FROM OTHER WEBSITES. THIS MOD IS ONLY OFFICIALLY UPLOADED TO CURSEFORGE.


![Logo](logo-banner.png)

___

[![CurseForge](https://img.shields.io/curseforge/dt/375088?logo=curseforge&label=Curseforge&labelColor=333333&color=%23ff6a00)](https://www.curseforge.com/minecraft/mc-mods/dragon-mounts-legacy)
[![Modrinth](https://img.shields.io/modrinth/dt/G3EPcczP?logo=modrinth&label=%20Modrinth&labelColor=333333)](https://modrinth.com/mod/dragon-mounts-legacy)
[![Support me on Patreon](https://img.shields.io/badge/dynamic/json?logo=Patreon&logoColor=f96854&style=flat&color=f96854&label=Patreon&labelColor=052d49&query=data.attributes.patron_count&url=https%3A%2F%2Fwww.patreon.com%2Fapi%2Fcampaigns%2F5686478?)](https://patreon.com/kaynien)

GitHub Repository for the Dragon Mounts: Legacy Minecraft Mod.

> "A Minecraft mod that allows you to breed dragon eggs and foster them to ridable dragons."
>
> BarracudaATA

> Dragon Mounts by Barracuda can be found [here](https://www.minecraftforum.net/forums/mapping-and-modding-java-edition/minecraft-mods/wip-mods/1439594-dragon-mounts-r46-wip),
with the github repo [here](https://github.com/ata4/dragon-mounts).
