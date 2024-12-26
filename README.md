<img src="./images/catroom.png" height="160" alt="CatRoom" align="right">

# CatRoom

CatRoom is a Cleanroom+Bukkit+Spigot server software forked from [CatServer](https://github.com/Luohuayu/CatServer).

## Features:

- Replaced Forge with Cleanroom
- Enhanced mod compatibility
- Built-in Forge-Bukkit permission bridge
- Make use of modern Java features
- Optimized plugin performance

For all fixes, see [fixed upstream issues](FIXED_UPSTREAM_ISSUES.md)

## Components:

- Minecraft Coder Pack
- CleanroomLoader (Continuation + Revamp of ForgeModLoader)
- Cleanroom Minecraft (Continuation + Revamp of MinecraftForge)
- Customized Mixin
- Bytecode Patcher (Coming Soon) \[Inspired by [Bansoukou](https://github.com/LoliKingdom/Bansoukou) and [Bytecode Patcher](https://github.com/jbredwards/Bytecode-Patcher)]
- [Fugue](https://github.com/CleanroomMC/Fugue), a mod patches many incompatibilities.
- Javassist
- [Scalar](https://github.com/CleanroomMC/Scalar/releases/tag/2.11.1), a Scala provider. We made Scala libraries become a standalone mod so it can be updated.

## Build Instructions:

1. Clone this repository
2. Import the `build.gradle` into your IDE (most preferably IntelliJ IDEA)
3. Once the import has finished, run `gradlew setup`
4. Build with `gradlew build`

## Development Tips:

- Only modify `projects/cleanroom/src/` directory if you want to change vanilla
- Run `gradlew genPatches` before commit, or the changes won't exist
- Modifications on `src/` doesn't need generating patches
- [Tips from Forge](https://github.com/MinecraftForge/MinecraftForge/wiki/If-you-want-to-contribute-to-Forge) are still apply, keep the patches clean!
- The current patches is full of useless hunks after we switched to VineFlower, we encourage contributors to manual clean up their patches

## Mod Development:

There's an unofficial [template](https://github.com/kappa-maintainer/ExampleMod-1.12.2-FG5) exist. Note: You need to build before run.

A porting guide is available in [Cleanroom wiki](https://cleanroommc.com/wiki/cleanroom-mod-development/introduction).

## Roadmap flow chart

```mermaid
graph TD;
    A(Mixin integration)-->D(Bouncepad overhaul - we are here);
    B(LWJGL compat)-->D;
    C(Newer Java compat)-->D;
    D-->E(Config any time);
    D-->G(Minor improvement and fixes)
    E-->F(Greater improvement needs configs)
    X(Cleanroom Gradle)-->D
    D-->X
    D-->Y(Better Mixin Integration)
    Y-->D
```
