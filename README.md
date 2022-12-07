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

- Download Vespucci-Festival
- Download httpmanager
- Download pmms

Add the following to your server.cfg:

```lua
ensure Vespucci-Festival
ensure httpmanager
exec @pmms/permissions.cfg
ensure pmms
```
By default, PMMS is set to admin only access, you can change this in the `permissions.cfg` provided with it, if you would prefer all players can access it. You will need to the read pmms installation instructions on the GitHub repository.

Please also read the installation instructions of httpmanager

------------------------------

# Recommendation

Open pmms > config.lua and change these values, so that ther Festival Screen audio can be heard from the pier making it a little more realistic:

```lua
Config = {}

-- Whether the game is RDR2 or GTA V
Config.isRDR = IsDuplicityVersion() and GetConvar("gamename", "gta5") == "rdr3" or not TerraingridActivate

-- Max distance at which inactive media player entities appear
Config.maxDiscoveryDistance = 80.0

-- Default sound attenuation multiplier when in the same room
Config.defaultSameRoomAttenuation = 0.0

-- Default sound attenuation multiplier when in a different room
Config.defaultDiffRoomAttenuation = 4.0

-- Default range where active media players are visible/audible
Config.defaultRange = 80.0

-- Maximum range that players can set
Config.maxRange = 400.0

-- Difference between the base volume in the same room and a different room
Config.defaultDiffRoomVolume = 0.25

-- Whether the filter options is enabled by default
Config.enableFilterByDefault = Config.isRDR

-- Default size for the NUI video screen
Config.defaultVideoSize = 30
```

Scroll down and find `Config.audioVisualizations = {` and paste in the following

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
		colors = {"#ee188c", "#176bed", "#16ec6d", "#5ffd1e", "#dcaa0a"} -- 5 Colours diffRoom, Left To Right
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
		colors = {"#ee188c", "#176bed", "#16ec6d", "#5ffd1e", "#dcaa0a"} -- 5 Colours diffRoom, Left To Right
	},
	["flower blocks"] = {
		name = "Blocky Flower"
	},
	["orbs"] = {
		name = "Orbs",
		colors = {"#ee188c","#7611f7"} -- diffRoom 2 Colours 
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

This will colourise the audio visualisations. You can of course change them yourself if you want to.

I have also provided the `defaultMediaPlayers.json` file which you will need to put inside pmms, this configures the Festival Beach screen for you.
