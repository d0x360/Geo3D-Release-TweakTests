# Geo3D - Geometric 3D inside ReShade
You need the following
- ReShade with addon support (http://reshade.me)
- Latest Geo3D release

Geo3D supports DirectX 9-12 which wouldn't be possible without ReShade's Api.
In the background is my disassembler fix and my assembler.
The first part of 2022 laid the groundwork for my recent quick progress in ReShade.
Support me on patreon here: http://patreon.com/Flugan

# Installation
Start with downloading the latest addon ReShade from http://reshade.me

Then you can use 7-zip to unpack reshade. Extract Geo3D and place reshade into the folders.

After moving reshade into the Geo3D folders rename both reshade32.dll and reshade64.dll into dxgi.dll for each folder.

For DirectX 9 games this has to be renamed again to d3d9.dll.

Be careful with existing ReShade installations. Copy the Geo3D section into the existing reshade.ini.

You probably want to keep your existing ReShade preset and need to get 3DToElse.fx into a suitable place by adjusting the preset in-game.

Install either the 32-bit or 64-bit version of Geo3D in the game folder together with reshade from before.

The real exe is often very large and often found in a binary subfolder so don't be surprised if it doesn't do anything in the root folder.

There are three values that affect 3D:
- Convergence
- Screen size
- Separation

Setting the right ScreenSize is very important. You can reduce separation to get a more comfortable experience with reduced depth.

Convergence is key to making the presentation less flat.

# Screen size
For physical screens this is simple as you can just measure the 16:9 diagonal in inches.

VR screens is harder but the default value of 220 is a good starting point.

Screen size should never be smaller than the actual screen.

# Separationon
At 100% the separation is max and far away objects will appear 6.5 cm apart on the screen. When the screen is close around 50% is recommended.

# Convergance
By default you have convergence=1. Going to convergence 2 pushes the virtual screen twice as far into the scene.

You can set StereoConvergence straight into the reshade.ini file. This is quick but hard to get right.

Instead of changing a single value you can define a range of values by adjusting ConvStart, ConvStep and ConvNum.

You can switch convergence by using ctrl-F3 and ctrl-F4. When you're done set ConvNum to zero! Otherwise convergence will reset to ConvStart at next launch.

Being able to see both images at the "same" time is key to knowing at what object is at screen depth. You can disable 3DToElse.fx shader to see both images.

# DXIL
A incomplete list of games using the new Shader Model 6+.

Setting "DXIL=1" inside reshade.ini allows convergence to change but could crash the game at this point of testing.
- Alan Wake Remastered
- Cyberpunk 2077
- Deathloop
- DIRT 5
- Elden Ring
- Evil Genius 2: World Domination
- F1 2021
- Far Cry 6
- Farming Simulator 22
- Forza Horizon 5
- Grid Legends
- Halo Infinite
- Hitman 3
- Horizon Zero Dawn
- Judgement
- Lost Judgement
- Marvel's Guardians of the Galaxy
- Marvel's Spider-Man Remastered
- Metro Exodus: Enhanced Edition
- Monster Hunter Rise
- Path of Exile
- Resident Evil 2 (2019)
- Resident Evil 3 (2020)
- Resident Evil 7
- Resident Evil Village
- Star Wars Battlefront II (2017)
- The Riftbreaker
- Zombie Army 4: Dead War

Optonal software
- VRScreenCap (https://github.com/artumino/VRScreenCap)

VRScreenCap uses VRExport addon in DX11 & 12 to expose full resolution SBS images
