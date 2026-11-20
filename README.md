# Modes-for-minecraft-and-stuff
A Minecraft mod for **Fabric 1.20.1** that adds rubies to the game.
# RubyCraft

A Minecraft mod for **Fabric 1.20.1** that adds rubies to the game.

## Features

- **Ruby Ore** that generates underground (Y -64 to 16), drops rubies and supports Fortune
- **Ruby** gem and **Block of Ruby** (craftable both ways)
- **Healing Charm**: right-click to heal and gain Regeneration (16 uses, 10 second cooldown)
- **Custom creative tab** with all mod items
- **/sethome** and **/home** commands to save and teleport to a home point, even across dimensions

## Building

Requirements: JDK 17 and Gradle (or open the project in IntelliJ IDEA, which sets everything up).

```bash
gradle wrapper      # one time, generates ./gradlew
./gradlew build     # jar appears in build/libs/
./gradlew runClient # launch Minecraft with the mod
```

## Installing

1. Install [Fabric Loader](https://fabricmc.net/use/) for Minecraft 1.20.1
2. Put [Fabric API](https://modrinth.com/mod/fabric-api) and the RubyCraft jar into the `mods` folder

## Project structure

```
src/main/java/dev/rubycraft/
  RubyCraft.java          entry point
  block/ModBlocks.java    blocks and block items
  item/ModItems.java      items
  item/HealingCharmItem.java
  item/ModItemGroups.java creative tab
  command/ModCommands.java /sethome and /home
  world/ModWorldGen.java  ore generation hook
src/main/resources/
  assets/                 models, textures, lang
  data/                   recipes, loot tables, worldgen, tags
```

## Roadmap

- [ ] Ruby tools and armor
- [ ] Persistent homes saved to disk
- [ ] Ruby golem mob

## License

MIT
