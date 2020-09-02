# Creative Music Sound System / Game Blaster information for MiSTer ao486 core

Information on how to get CMS/GB sound working on compatible games on the MiSTer ao486 core.

**If you know of any other game that works, or how to get it to work, please dont hesitate to contact me in at the [MiSTer FPGA forum](https://misterfpga.org/viewforum.php?f=13) (chimaera).**

Most information has been gathered from these sources:

* [Nerdly Pleasures](https://nerdlypleasures.blogspot.com/2012/10/all-you-ever-wanted-to-know-about.html)
* [VOGONS.org](https://www.vogons.org/viewtopic.php?t=58927)

_ _ _

## General Tips

For the majority of the games that support CMS, it is only needed to configure the game correctly via the SETUP/INSTALL/CONFIG.
For some games, it is required to pass on commands to the main EXE. I have created .BATs for these games, look in the Files/Game BATs folder.

If you cannot get CMS sound to work on any of the games listed as CONFIRMED WORKING, then it could be one of several problems:

1. Sound drivers were not shipped at release, but released later (mostly Sierra games). Check install directory for files with CMS in it. I have included the drivers I found in the Files/Game Drivers folder.

2. Some games doesn't install all sound drivers to hdd when installed, but only the chosen sound driver. Try to reinstall and choose the Creative Music System / Game Blaster driver.

3. The game uses an autodetection scheme that overides chosen driver, it often chooses Adlib instead of CMS. If this is the case, then you'll need to patch out the autodetection. Luckily, most of those games are patched in this project: [VOGONS.org](https://www.vogons.org/viewtopic.php?t=58927). I have included the patches in the Files/Game Patches folder.

5. Some games require you to run the CMSDRV.COM/SBC-CMS.COM driver before launching the game. The driver can be unloaded by adding /U command when relaunching the driver. Drivers can be found in the Files/System Drivers folder.

6. If none of above options work, then you probably have the wrong version of the game.

_ _ _

## Games List - Sound CONFIRMED WORKING

**A**
* Airball (1987) by MicroDeal
    * ´´´AIRBALL.EXE /CMS´´´

* Altered Destiny (1990) by Accolade
    * Patch needed to remove autodetection: ´´´EXE.EXE at HEX 1910E | 75 --> 74´´´ (patch by CarlosTex)

* Arkanoid: Revenge of DOH (1989) by Taito
    * Special Edition only
    * Delete ´´´DOH.CFG´´´ and run ´´´DOH.EXE R´´´



**B**
* Bad Blood (1990) by ORIGIN
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz
* Battle Chess II: Chinese Chess (1990) by Interplay
    * Only SFX

* BattleTech: The Crescent Hawks' Revenge (1990) by Westwood
    * Only SFX

* Bubble Bobble (1986) by Taito
    * Delete ´´´BUBBOB.CFG´´´ and run ´´´BUBBLE.EXE R´´´

* Budokan: The Martial Spirit (1989) by Electronic Arts
    * ´´´BUDO.COM CMS´´´



**C**
* Castle of Dr. Brain (1991) by Sierra On-Line
* Champions of Krynn (1990) by Strategic Simulations
    * Delete ´´´KRYNN.CFG´´´ and run game

* Chuck Yeager's Air Combat (1991) by Electronic Arts
* Code-Name Iceman (1989) by Sierra On-Line
* Conan: The Cimmerian (1991) by Synergistic Software
    * Some versions are missing CMS.DRV from

* Conquests of Camelot - The Search for the Grail (1990) by Sierra On-Line
* Conquests of the Longbow - The Legend of Robin Hood (1991) by Sierra On-Line



**D**
* Day of the Viper (1990) by Accolade
    * Patch needed to set CMS: ´´´VIPER.EXE at HEX 139D3 | FF --> 02´´´ (patch by NewRisingSun)
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
    * Patch needed to set CMS: ´´´MAIN at HEX 28B | 0F --> 02´´´ (patch by NewRisingSun)

* Gunboat (1990) by Accolade
    * Patch needed to set CMS: ´´´GB.EXE at HEX 216D | 0F --> 02´´´ (patch by NewRisingSun)
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
    * All VGA versions, run ´´´INDY256.EXE G´´´
    * Only EGA version 1.4, run ´´´INDY3.EXE GAMEB´´´
    * Adlib option seems to crash? ´´´Integer divided by 0´´´
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz




**J**
* J.R.R. Tolkien's The Lord of the Rings, Vol. I (1990) by Interplay
    * SFX Only

* Jack Nicklaus' Unlimited Golf & Course Design (1990) by Sculptured Software
    * ´´´GOLF.EXE CMS´´´

* Joe Montana Football (1990) by SEGA
    * Ingame Option

* Jones in the Fast Lane (1991) by Sierra On-Line



**K**
* Keef the Thief: A Boy and His Lockpick (1989) by Naughty Dog
    * Need to install the game with CMS option to get CMS driver file ´´´CKEEF.SMB´´´
* King's Quest (1990) by Sierra On-Line
    * SCI version only, not AGI
* King's Quest IV - The Perils of Rosella (1988) by Sierra On-Line
* King's Quest V - Absence Makes the Heart Go Yonder! (1990) by Sierra On-Line



**L**
* Lakers versus Celtics and the NBA Playoffs (1989) by Electronic Arts
    * SFX Only?
    * ´´´NBA.EXE CMS´´´

* Laura Bow 1: The Colonel's Bequest (1989) by Sierra On-Line
* Laura Bow 2: The Dagger of Amon Ra (1992) by Sierra On-Line
* Leisure Suit Larry 1: In the Land of the Lounge Lizards (1991) by Sierra On-Line
    * VGA version only

* Leisure Suit Larry: Goes Looking for Love (In Several Wrong Places) (1988) by Sierra On-Line
* Leisure Suit Larry 3: Passionate Patti in Pursuit of the Pulsating Pectorals (1989) by Sierra On-Line
* Leisure Suit Larry 5: Passionate Patti Does a Little Undercover Work (1991) by Sierra On-Line
* Les Manley: in Search for the King (1990) by Accolade
* Loom (1990) by Lucasfilm Games
    * ´´´LOOM.EXE G´´´



**M**
* Miami Vice (1989) by Capstone Software
    * ???? copy SBC-CMS.COM to CMSDRV.COM
* Mixed-Up Fairy Tales (1991) by Sierra On-Line
* Mixed-Up Mother Goose (1991) by Sierra On-Line
    * SCI and VGA version only, not AGI



**N**
* Night Shift (1990) by Attention to Detail Limited
    * ´´´IML.EXE G´´´
* NY Warriors (1991) by Synergistic Software



**O**
* Oil's Well (1990) by Banana Development
* Operation Wolf (1989) by Taito
    * Delete ´´´OWCONFIG.DAT´´´ and run ´´´WOLF.EXE R´´´



**P**
* Paku Paku (2011) by Paladin Systems North
    * ´´´PAKU.EXE /cms´´´

* PGA Tour Golf (1990) by Sterling Silver Software
    * Patch needed to remove autodetection: ´´´GOLF.EXE at HEX 267 | 0F --> 02´´´ (patch by NewRisingSun)

* Police Quest - In Pursuit of the Death Angel (1992) by Sierra On-Line
    * VGA only, not AGI

* Police Quest 2 - The Vengeance (1988) by Sierra On-Line
* Police Quest 3 - The Kindred (1991) by Sierra On-Line
* Power Drift (1990) by SEGA
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz

* Prince of Persia (1990) by Brøderbund Software
    * Version 1.0
    * ´´´PRINCE.EXE Gblast´´´
    * Use ´´´POPKB.COM Gblast´´´ for sound correction on faster computers

* Puzznic (1990) by Taito
    * Delete ´´´CONFIG.DAT´´´ and run ´´´PUZZNIC.EXE R´´´



**Q**
* QIX (1989) by Taito
    * Delete ´´´CONFIG.DAT´´´ and run ´´´QIX.COM R´´´

* Quest for Glory I - So You Want To Be A Hero (1992) by Sierra On-Line
* Quest for Glory II - Trial by Fire (1990) by Sierra On-Line



**R**
* Rambo III (1989) by Taito
    * Delete ´´´CONFIG.DAT´´´ and run ´´´RAMBO.EXE R´´´

* Rastan (1990) by Taito
    * Delete ´´´CONFIG.DAT´´´ and run ´´´RASTAN.EXE R´´´



**S**
* Secret of Monkey Island, The (1990) by Lucasfilm Games LLC
    * ´´´MONKEY.COM G´´´
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz

* Shanghai II - Dragon's  Eye (1990) by Activision
* Silpheed (1989) by Game Arts Co
    * Only version 2.2 and up

* Sorcerian (1991) by Nihon Falcom Corp.
* Space Quest - The Sarien Encounter (1991) by Sierra On-Line
    * SCI version only, not AGI
* Space Quest III - The Pirates of Pestulon (1989) by Sierra On-Line
* Space Quest IV - Roger Wilco and the Time Rippers (1991) by Sierra On-Line
* Spirit of Excalibur (1990) by Synergistic Software
    * The game doesn't seem to like fast CPU speeds, use a slowdown program to set speed to 25Mhz

* Spot (1991) by Virgin
* Star Control (1990) by Toys for Bob
    * Patch needed to remove autodetection: ´´´GOLF.EXE´´´ (patch by Scali)
        * ´´´HEX 685D | 74 26 --> 90 90´´´
        * ´´´HEX 6870 | 75 E2 --> 90 90´´´
    * ´´´STARCON.EXE /S:CMS´´´

* Stormovik SU-25 - Soviet Attack Fighter (1990) by Electronic Arts
    * ´´´SU25.EXE CMS´´´

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
    * ´´´WIND.EXE CMS´´´

* Wolf Pack (1990) by NovaLogic
    * ´´´WOLFPACK.EXE R´´´ (not detected but works anyway)

_ _ _

## Games List - Sound NOT WORKING CORRECTLY

**B**
* Breach 2 (1990) by Omnitrend Software
    * Autodetect conflict? Probably needs to be patched.
    * Game works with sound in DOSBOX with sbtype=gb, but not sbtype=sb2 as the games in WORKING category



**D**
* Death Knights of Krynn (1991) by Strategic Simulations
    * Autodetect conflict? Probably needs to be patched.
    * Game works with sound in DOSBOX with sbtype=gb, but not sbtype=sb2 as the games in WORKING category

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
