# Vespucci Festival ⛱️🎵

Inspired by [Faswan Festival (Hypnonema Compatible)](https://forum.cfx.re/t/free-faswan-festival-hypnonema-compatible/4904994), Vespucci Festival is a free map created by [TayMcKenzieNZ](https://github.com/TayMcKenzieNZ) located in Vespucci Beach, just in front of the local skatepark. 

Entertain your city with a FREE music festival map by either playing real life LIVE radio stations, Twitch stream your IRL DJing, or play YouTube videos!

**The map requires [PMMS FiveM / RedM synchronized media player by Kibook](https://github.com/kibook/pmms) for all screens to syncronize.**




# Dependencies

- [httpmanager by Kibook](https://github.com/kibook/httpmanager)

- [PMMS FiveM / RedM synchronized media player by Kibook](https://github.com/kibook/pmms)

- Latest Server Artifacts for [Windows](https://runtime.fivem.net/artifacts/fivem/build_server_windows/master/) or [Linux](https://runtime.fivem.net/artifacts/fivem/build_proot_linux/master/)

------------------------------

# Installation

- Download Vespucci-Festival and drag the Vespucci-Festival folder into your server
- Download httpmanager
- Download pmms
- Open the `PMMS Festival Screen Config` folder and copy the files over to the `pmms` resource folder


Add the following to your server.cfg:

```lua
ensure Vespucci-Festival
ensure httpmanager
exec @pmms/permissions.cfg
ensure pmms
```
**By default, PMMS is set to admin only access, you can change this in the `permissions.cfg` provided with it, if you would prefer all players can access it. You will need to the read pmms installation instructions on the GitHub repository.**

Please also read the installation instructions of httpmanager

------------------------------

# PMMS

I have provided files for PMMS which will change the values and settings, so that the Festival Screen audio can be heard from the pier making it a little more realistic. I have also provided some default radio stations that you can select in the UI of PMMS, to use if you wish to play those, on the festival screen, or inside your vehicle. They are examples, and you can of course add your own.

In the config file, I have set up the audio vislualizations for you and have marked out how many colours each one supports. You can of course change these if you wish to. Colours support names and/or hex codes

```lua
Config.audioVisualizations = {
	["bars"] = {
		name = "Bars"
	},
	["bars blocks"] = {
		name = "Blocky Bars"
	},
	["cubes"] = {
		name = "Cubes",
		colors = {"orange", "aqua", "blue", "purple"} -- Order bottom to top. Maximum 4 Colours 
	},
	["dualbars"] = {
		name = "Dual Bars",
		colors = {"#ee188c", "#176bed", "#16ec6d", "#5ffd1e", "#dcaa0a"} -- 5 Colours, Left To Right
	},
	["dualbars blocks"] = {
		name = "Blocky Dual Bars"
	},
	["fireworks"] = {
		name = "Fireworks",
		colors = {"#ee188c"} -- Maximum 1 Colour 
	},
	["flower"] = {
		name = "Flower",
		colors = {"#ee188c", "#176bed", "#16ec6d", "#5ffd1e", "#dcaa0a"} -- 5 Colours, Left To Right
	},
	["flower blocks"] = {
		name = "Blocky Flower"
	},
	["orbs"] = {
		name = "Orbs",
		colors = {"#ee188c","#7611f7"} -- 2 Colours 
	},
	["ring"] = {
		name = "Ring"
	},
	["rings"] = {
		name = "Rings"
	},
	["round wave"] = {
		name = "Round Wave"
	},
	["shine"] = {
		name = "Shine"
	},
	["shine rings"] = {
		name = "Shine Rings",
		colors = {"#ee188c", "#176bed", "#16ec6d", "#5ffd1e", "#dcaa0a"}
	},
	["shockwave"] = {
		name = "Shockwave"
	},
	["star"] = {
		name = "Star"
	},
	["static"] = {
		name = "Static"
	},
	["stitches"] = {
		name = "Stitches"
	},
	["web"] = {
		name = "Web"
	},
	["wave"] = {
		name = "Wave"
	}
}
```


