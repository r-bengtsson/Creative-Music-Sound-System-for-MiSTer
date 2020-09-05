# Creative Music Sound System / Game Blaster information for MiSTer ao486 core

Information on how to get CMS/GB sound working on compatible games on the MiSTer ao486 core.

**If you know of any other game that works, or how to get it to work, please dont hesitate to contact me in at the [MiSTer FPGA forum](https://misterfpga.org/viewtopic.php?f=13&t=1118) (chimaera).**

Most information has been gathered from these sources:

* [Nerdly Pleasures](https://nerdlypleasures.blogspot.com/2012/10/all-you-ever-wanted-to-know-about.html)
* [VOGONS.org](https://www.vogons.org/viewtopic.php?t=58927)

_ _ _

## General Tips

For the majority of the games that support CMS, it is only needed to configure the game correctly via the SETUP/INSTALL/CONFIG (this is true for all games without any extra information in the list).
For some games, it is required to pass on commands to the main EXE. I have created .BATs for these games, look in the [Files/Game BATs folder](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/tree/master/Files/Game%20BATs).

If you cannot get CMS sound to work on any of the games listed as CONFIRMED WORKING, then it could be one of several problems:

1. Sound drivers were not shipped at release, but released later (mostly Sierra games). Check install directory for files with CMS in it. I have included the drivers I found in the [Files/Game Drivers folder](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/tree/master/Files/Game%20Drivers).

2. Some games doesn't install all sound drivers to hdd when installed, but only the chosen sound driver. Try to reinstall and choose the Creative Music System / Game Blaster driver.

3. The game uses an autodetection scheme that overides chosen driver, it often chooses Adlib instead of CMS. If this is the case, then you'll need to patch out the autodetection. Luckily, most of those games are patched in this project: [VOGONS.org](https://www.vogons.org/viewtopic.php?t=58927). I have included the patches in the [Files/Game Patches folder](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/tree/master/Files/Game%20Patches).
**REMEMBER TO MAKE BACKUP OF YOUR ORIGINAL FILES**

5. Some games require you to run the CMSDRV.COM/SBC-CMS.COM driver before launching the game. The driver can be unloaded by adding /U command when relaunching the driver. Drivers can be found in the [Files/System Drivers folder](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/tree/master/Files/System%20Drivers).

6. If none of above options work, then you probably have the wrong version of the game.

_ _ _


## Creative Music System and the Miles Sound System

A user named Tronix on the Vogons forum has made a midi driver using the Miles Sound System drivers to make alot more games compatible with the CMS.
It involves a little more work to get those games working.
Checkout the link below to see an example:

* [Warcraft 2](https://www.youtube.com/watch?v=RM3cuSSXbrE)

You can find more information about that in the [VOGONS.org forum](https://www.vogons.org/viewtopic.php?f=24&t=43553&p=423974).

I have saved the CMS MSS drivers in the Files / System Drivers folder for preservation.

_ _ _

## Games List - Sound CONFIRMED WORKING

**A**
* Airball (1987) by MicroDeal
    * Only SFX
    * `AIRBALL.EXE /CMS`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Airball%20(1987).zip)

* Altered Destiny (1990) by Accolade
    * Patch needed to remove autodetection: `EXE.EXE at HEX 1910E | 75 --> 74` (patch by CarlosTex)
    * [Download Patch](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Patches/Altered%20Destiny%20(1990).zip)

* Arkanoid: Revenge of DOH (1989) by Taito
    * Special Edition only
    * Delete `DOH.CFG` and run `DOH.EXE R`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Arkanoid%20-%20Revenge%20of%20DOH%20%5BSpecial%20Edition%5D%20(1989).zip)



**B**
* Bad Blood (1990) by ORIGIN
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz

* Battle Chess II: Chinese Chess (1990) by Interplay
    * Only SFX

* BattleTech: The Crescent Hawks' Revenge (1990) by Westwood
    * Only SFX

* Bubble Bobble (1986) by Taito
    * Delete `BUBBOB.CFG` and run `BUBBLE.EXE R`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Bubble%20Bobble%20(1986).zip)

* Budokan: The Martial Spirit (1989) by Electronic Arts
    * `BUDO.COM CMS`
    [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Budokan%20-%20The%20Martial%20Spirit%20(1989).zip)



**C**
* Castle of Dr. Brain (1991) by Sierra On-Line
    * [Download Updated SB Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Castle%20of%20Dr.%20Brain%20(1991).zip)
* Champions of Krynn (1990) by Strategic Simulations
    * Delete `KRYNN.CFG` and run game
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Champions%20of%20Krynn%20(1990).zip)

* Chuck Yeager's Air Combat (1991) by Electronic Arts
* Code-Name Iceman (1989) by Sierra On-Line
* Conan: The Cimmerian (1991) by Synergistic Software
    * Some versions are missing CMS.DRV
    * [Download CMS Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Conan%20-%20The%20Cimmerian%20(1991).zip)

* Conquests of Camelot - The Search for the Grail (1990) by Sierra On-Line
* Conquests of the Longbow - The Legend of Robin Hood (1991) by Sierra On-Line



**D**
* Day of the Viper (1990) by Accolade
    * Patch needed to set CMS: `VIPER.EXE at HEX 139D3 | FF --> 02` (patch by NewRisingSun)
    * [Download Patch](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Patches/Day%20of%20the%20Viper%20(1990).zip)
    * Adlib needs Sound Blaster Drivers
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz

* Don't Go Alone (1989) by Sterling Silver Software



**E**
* EcoQuest: The Search for Cetus (1991) by Sierra On-Line
* Elvira (1990) by Horror Soft



**F**
* F-14 Tomcat (1990) by Activision
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz



**G**
* Game of Harmony, The (1990) by Assembly Line
    * NOT E-Motion
    * Patch needed to set CMS: `MAIN at HEX 28B | 0F --> 02` (patch by NewRisingSun)
    * [Download Patch](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Patches/Game%20of%20Harmony%2C%20The%20(1990).zip)

* Gunboat (1990) by Accolade
    * Patch needed to set CMS: `GB.EXE at HEX 216D | 0F --> 02` (patch by NewRisingSun)
    * [Download Patch](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Patches/Gunboat%20(1990).zip)
    * Adlib needs Sound Blaster Drivers
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz



**H**
* Hero's Quest: So You Want to Be a Hero (1989) by Sierra On-Line
* Hoyle: Official Book of Games - Volume 1 (1989) by Sierra On-Line
* Hoyle: Official Book of Games - Volume 2 (1990) by Sierra On-Line
* Hoyle: Official Book of Games - Volume 3 (1991) by Sierra On-Line
    * VGA Version, EGA has option but doesn't work?



**I**
* Indiana Jones and the Last Crusade: The Graphic Adventure (1989) by Lucasfilm Games
    * All VGA versions, run `INDY256.EXE G`
    * [Download .BAT (VGA)](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Indiana%20Jones%20and%20the%20Last%20Crusade%20-%20The%20Graphic%20Adventure%20%5BVGA%5D%20(1989).zip)
    * Only EGA version 1.4, run `INDY3.EXE GAMEB`
    * [Download .BAT (EGA)](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Indiana%20Jones%20and%20the%20Last%20Crusade%20-%20The%20Graphic%20Adventure%20%5BEGA%5D%20v1.4%20(1989).zip)
    * Adlib option seems to crash? `Integer divided by 0`
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz




**J**
* J.R.R. Tolkien's The Lord of the Rings, Vol. I (1990) by Interplay
    * SFX Only

* Jack Nicklaus' Unlimited Golf & Course Design (1990) by Sculptured Software
    * `GOLF.EXE CMS`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Jack%20Nicklaus'%20Unlimited%20Golf%20%26%20Course%20Design%20(1990).zip)

* Joe Montana Football (1990) by SEGA
    * Ingame Option

* Jones in the Fast Lane (1991) by Sierra On-Line
    * [Download CMS Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Jones%20in%20the%20Fast%20Lane%20(1991).zip)



**K**
* Keef the Thief: A Boy and His Lockpick (1989) by Naughty Dog
    * Need to install the game with CMS option to get CMS driver file `CKEEF.SMB`
    * [Download CMS Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Keef%20the%20Thief%20-%20A%20Boy%20and%20His%20Lockpick%20(1989).zip)
* King's Quest (1990) by Sierra On-Line
    * SCI version only, not AGI
* King's Quest IV - The Perils of Rosella (1988) by Sierra On-Line
    * [Download CMS Driver (SCI v0.111)](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/King's%20Quest%20IV%20-%20The%20Perils%20of%20Rosella%20%5BSCI%5D%20v0.111%20(1988).zip)
    * [Download CMS Driver (SCI v6.004)](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/King's%20Quest%20IV%20-%20The%20Perils%20of%20Rosella%20%5BSCI%5D%20v6.004%20(1988).zip)
* King's Quest V - Absence Makes the Heart Go Yonder! (1990) by Sierra On-Line



**L**
* Lakers versus Celtics and the NBA Playoffs (1989) by Electronic Arts
    * SFX Only?
    * `NBA.EXE CMS`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Lakers%20versus%20Celtics%20and%20the%20NBA%20Playoffs%20(1989).zip)

* Laura Bow 1: The Colonel's Bequest (1989) by Sierra On-Line
    * [Download CMS Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Laura%20Bow%201%20-%20The%20Colonel's%20Bequest%20(1989).zip)

* Laura Bow 2: The Dagger of Amon Ra (1992) by Sierra On-Line
* Leisure Suit Larry 1: In the Land of the Lounge Lizards (1991) by Sierra On-Line
    * VGA version only, not AGI
    * [Download CMS Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Leisure%20Suit%20Larry%201%20In%20the%20Land%20of%20the%20Lounge%20Lizards%20%5BVGA%5D%20v2.1%20(1991).zip)

* Leisure Suit Larry: Goes Looking for Love (In Several Wrong Places) (1988) by Sierra On-Line
    * [Download CMS Driver (v0.011)](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Leisure%20Suit%20Larry%20Goes%20Looking%20for%20Love%20(In%20Several%20Wrong%20Places)%20v0.011%20(1988).zip)
    * [Download CMS Driver (v2.000)](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Leisure%20Suit%20Larry%20Goes%20Looking%20for%20Love%20(In%20Several%20Wrong%20Places)%20v2.000%20(1988).zip)

* Leisure Suit Larry 3: Passionate Patti in Pursuit of the Pulsating Pectorals (1989) by Sierra On-Line
* Leisure Suit Larry 5: Passionate Patti Does a Little Undercover Work (1991) by Sierra On-Line
* Les Manley: in Search for the King (1990) by Accolade
    * [Download CMS Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Les%20Manley%20in%20Search%20for%20the%20King%20(1990).zip)

* Loom (1990) by Lucasfilm Games
    * `LOOM.EXE G`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Loom%20(1990).zip)



**M**
* Miami Vice (1989) by Capstone Software
    * ???? copy SBC-CMS.COM to CMSDRV.COM
* Mixed-Up Fairy Tales (1991) by Sierra On-Line
* Mixed-Up Mother Goose (1991) by Sierra On-Line
    * SCI and VGA version only, not AGI



**N**
* Night Shift (1990) by Attention to Detail Limited
    * `IML.EXE G`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Night%20Shift%20(1990).zip)
* NY Warriors (1991) by Synergistic Software



**O**
* Oil's Well (1990) by Banana Development
* Operation Wolf (1989) by Taito
    * Delete `OWCONFIG.DAT` and run `WOLF.EXE R`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Operation%20Wolf%20(1989).zip)



**P**
* Paku Paku (2011) by Paladin Systems North
    * `PAKU.EXE /cms`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Paku%20Paku%20v1.6%20(2011).zip)

* PGA Tour Golf (1990) by Sterling Silver Software
    * Patch needed to remove autodetection: `GOLF.EXE at HEX 267 | 0F --> 02` (patch by NewRisingSun)
    * [Download Patch](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Patches/PGA%20Tour%20Golf%20(1990).zip)

* Police Quest - In Pursuit of the Death Angel (1992) by Sierra On-Line
    * VGA only, not AGI
    * [Download CMS Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Police%20Quest%20-%20In%20Pursuit%20of%20the%20Death%20Angel%20%5BVGA%5D%20(1992).zip)

* Police Quest 2 - The Vengeance (1988) by Sierra On-Line
    * [Download CMS Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Police%20Quest%202%20-%20The%20Vengeance%20(1988).zip)

* Police Quest 3 - The Kindred (1991) by Sierra On-Line
* Power Drift (1990) by SEGA
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz

* Prince of Persia (1990) by Brøderbund Software
    * Version 1.0
    * `PRINCE.EXE Gblast`
    * Use `POPKB.COM Gblast` for sound correction on faster computers
    * [Download POPKB + .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Patches/Prince%20of%20Persia%20v1.0%20(1990).zip)

* Puzznic (1990) by Taito
    * Delete `CONFIG.DAT` and run `PUZZNIC.EXE R`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Puzznic%20(1990).zip)



**Q**
* QIX (1989) by Taito
    * Delete `CONFIG.DAT` and run `QIX.COM R`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/QIX%20(1989).zip)

* Quest for Glory I - So You Want To Be A Hero (1992) by Sierra On-Line
* Quest for Glory II - Trial by Fire (1990) by Sierra On-Line



**R**
* Rambo III (1989) by Taito
    * Delete `CONFIG.DAT` and run `RAMBO.EXE R`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Rambo%20III%20(1989).zip)

* Rastan (1990) by Taito
    * Delete `CONFIG.DAT` and run `RASTAN.EXE R`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Rastan%20(1990).zip)



**S**
* Secret of Monkey Island, The (1990) by Lucasfilm Games LLC
    * `MONKEY.COM G`
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Secret%20of%20Monkey%20Island%2C%20The%20(1990).zip)

* Shanghai II - Dragon's  Eye (1990) by Activision
* Silpheed (1989) by Game Arts Co
    * Only version 2.2 and up

* Sorcerian (1991) by Nihon Falcom Corp.
* Space Quest - The Sarien Encounter (1991) by Sierra On-Line
    * SCI version only, not AGI
* Space Quest III - The Pirates of Pestulon (1989) by Sierra On-Line
    * [Download CMS Driver](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Drivers/Space%20Quest%20III%20-%20The%20Pirates%20of%20Pestulon%20v1.0U%20(1989).zip)

* Space Quest IV - Roger Wilco and the Time Rippers (1991) by Sierra On-Line
* Spirit of Excalibur (1990) by Synergistic Software
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz

* Spot (1991) by Virgin
* Star Control (1990) by Toys for Bob
    * Patch needed to remove autodetection: `STARCON.EXE` (patch by Scali)
        * `HEX 685D | 74 26 --> 90 90`
        * `HEX 6870 | 75 E2 --> 90 90`
    * `STARCON.EXE /S:CMS`
    * [Download Patch + .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20Patches/Star%20Control%20(1990).zip)

* Stormovik SU-25 - Soviet Attack Fighter (1990) by Electronic Arts
    * `SU25.EXE CMS`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Stormovik%20SU-25%20-%20Soviet%20Attack%20Fighter%20(1990).zip)

* Strike Aces (1990) by Vektor Grafix
    * NOT Fighter Bomber



**T**
* Test Drive III - The Passion (1990) by Accolade
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz

* Times of Lore (1989) by ORIGIN
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz



**U**
* Ultima VI - The False Prophet (1990) by ORIGIN
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 50Mhz



**V**
* Vengeance of Excalibur (1991) by Synergistic Software



**W**
* Windwalker (1990) by ORIGIN
    * `WIND.EXE CMS`
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Windwalker%20(1990).zip)

* Wolf Pack (1990) by NovaLogic
    * `WOLFPACK.EXE R` (not detected but works anyway)

_ _ _

## Games List - Sound NOT WORKING CORRECTLY

* Breach 2 (1990) by Omnitrend Software
    * Autodetect conflict? Probably needs to be patched.
    * Game works with sound in DOSBOX with sbtype=gb, but not sbtype=sb2 as the games in WORKING category

* Death Knights of Krynn (1991) by Strategic Simulations
    * Autodetect conflict? Probably needs to be patched.
    * Game works with sound in DOSBOX with sbtype=gb, but not sbtype=sb2 as the games in WORKING category
    * [Download .BAT](https://github.com/chimaera66/Creative-Music-Sound-System-for-MiSTer/blob/master/Files/Game%20BATs/Death%20Knights%20of%20Krynn%20(1991).zip)

_ _ _

## Games List - Games not really compatible (Perhaps not right versions?)

* Blue Max: Aces of the Great War (1990) by Three-Sixty Pacific
    * Box claims support but seems to be Adlib only

* Das Boot: German U-Boat Simulation (1990) by Three-Sixty Pacific
    * Box claims support but seems to be Adlib only

* Hoverforce (1990) by Millennium Interactive
* Jordan vs Bird: One on One (1988) by Electronic Arts
* Monte Carlo Baccarat (1991) by Capstone Software
* Sargon V: World Class Chess (1991) by Activision
* Secret of the Silver Blades (1990) by Strategic Simulations
* Stratego (1990) by Accolade
* Trump Castle II (1991) by Capstone Software
* Wing Commander II: Vengeance of the Kilrathi (1991) by ORIGIN
    * Probably labeled so in Moby because of Ultima VI / Wing Commander II compilation

* Xenocide (1990) by Micro Revelations
