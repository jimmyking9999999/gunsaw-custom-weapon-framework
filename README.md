# gunsaw-custom-weapon-framework
Mod to add custom weapon functionality into itch.io game Gunsaw, where anyone can add weapons to via a web-based modular .txt file system.
<img width="1200" height="630" alt="image" src="https://github.com/user-attachments/assets/40c13f6f-a5cd-425f-90bd-f00f74a479b8" />

# Mod Contents
## Custom Weapons!
- **Custom projectile-based weapons**
- Damage, speed, lifetime, knockback, crit multipliers
- Highly customizable projectile modifier scripts, including homing, fire, explosions, dynamic speed, ricochet, and specialized movement

**Custom melee weapons**
- Highly customizable melee modifiers, such as hitlag, multi-hit combos, swing and impact animations, and aiming

**Custom hitscan-based weapons**
- Bullet amounts, recoil, knockback, penetration, self-knockback multiplier, crit multiplier, laser and farsight

**Special flags and mechanics**
- Burst fire, which shoot a burst per click
- Weapon silencers, which do not alert enemies upon firing

**Customizable visuals**
- Customizable sprites for each weapon, projectile, visual effect, empty magazine weapon, magazine, etc..
- Custom VFX (on-hit, on-swing, line trails)
- Customizable sounds for shooting and reloading

**In-game integration**
- Full enemy integration, with enemies randomly potentially spawning with custom weapons 
- Simple variables allow control of basic enemy behavior (distance, firerate)
- In-game crates may drop your weapon based on the `powerlevel`

## Installation
Unlike my other Gunsaw Mod, Gunsaw Level Editor+, this mod requires a dedicated mod loader due to the much higher complexity. As such, it uses `BepInEx` in order to function

### Setting up BepInEx:

1. Install [BepInEx v.5.4.23.3](https://github.com/BepInEx/BepInEx/releases/download/v5.4.23.3/BepInEx_win_x64_5.4.23.3.zip)
2. Extract the .zip into the game's directory, where your Gunsaw.exe is located. 
For itch.io users, this is wherever you downloaded the game
For itch app users, this is in `~AppData\Roaming\itch\apps\gunsaw-demo`
3. Run Gunsaw.exe. Afterwards, you should see a BepInEx folder. Inside of it should be 5 folders, one of which is `plugins`
4. Extract the mod's .zip file into the `plugins` folder
5. Launch the game, and enjoy the custom weapons!

Video tutorial: https://streamable.com/bj7u84

```
The up-to-date mod installation is located here. Download the .zip on the top menu and extract!
```

## Creating your own weapon
To help with creating your own custom weapon, I have created a handy browser page at https://gunsaw-weapon-creator.web.app

### Steps:
1. Choose a base weapon to clone from. This allows the fallback values be equal to the weapon. I.e. if you chose a pistol as a fallback weapon and did not fill out the magazine size on the website, it would default to a pistol's magazine size, or 12.

2. Choose a name! It will display in-game as said name

3. Optionally, choose an image. Imagine should be around 30x30 pixels maximum, and higher resolutions will automatically get scaled down in-game to the 30x30. This may look bad, thus pixel art is preferred

4. Choose the type of weapon for your gun. The easiest and most common is a hitscan weapon, like the majority of in-game weapons. Projectile weapons and melee weapons are custom weapon frames that are added through the mod, and configuration may be more difficult

5. Every other form is optional! Go wild, make a weapon and experiment!

6. When finished, click `Generate files` for a weapon file, and potentially a projectile file. Simply download and drag these files and any images into your `plugins/CustomWeapons` folder alongside the default custom weapons, and see it in-game!

-----------------------------

Alternatively, you can instead choose to edit pre-existing files in the `CustomWeapons` folder to test out what each thing does. This is a much simpler way of editing weapons, without needing to add weapon sprites
- The default weapon stats can be found on the [website](https://gunsaw-weapon-creator.web.app/), under the `network` tab as Weaponname.txt. For an assault rifle, that would be https://gunsaw-weapon-creator.web.app/WeaponData/Assault%20rifle.txt
- `TemplateWeapon.txt` is a text file that showcases what each non-custom script stat does, for manual file weapon creation

## Bugs
- Tinnitus volume may be loud for multiple explosions. For now, lower the volume in the pause menu
- Screenshake may be violent for multiple explosions
- Projectile ricochet may not bounce and instead do a 360* turn

## Planned Features
- Charge weapons. Hold to charge and lift to fire
- Particles, enhanced lightning

## FAQ
- Help! Why can't I see my weapon in-game?
  
There is probably an error with your weapon configuration files. 

To debug, enable BepInEx logging by opening `gunsaw-demo\BepInEx\config\BepInEx.cfg` and editing the `[Logging.Console]` `Enabled` from `false` to `true`

Open starting gunsaw, a console will open alongside the app, displaying potential errors

- Help! My game crashed!
  
Uh-oh. Report it here and I'll try to fix it ASAP!

- **How can I access my weapons in-game?**

`P` and `Ctrl + P` allow you to inject a random weapon into your inventory, or spawn one into the air for testing purposes!

## Credits
- @.redsphere., for working on the mod's framework with me early on and providing valuable feedback and testing, and actually kicking the project off
- @ae1oured, for creating half of the weapons and art you see in the mod
- Two placeholder images from the terraria Calamity mod weapons
- Sounds from pixabay and VFX from itch.io's Pixel FX Designer

