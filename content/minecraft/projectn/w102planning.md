---
title: "Project N Planning"
description: ""
summary: ""
date: 2024-10-08T19:53:05+08:00
lastmod: 2024-10-08T19:53:05+08:00
draft: false
weight: 102
toc: false
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

### Project Map

![map](images/minecraft/planning/wholemap1.png)

### Main Island

![main](images/minecraft/planning/main_island.png)

A populus island with smooth blending between different theme of cities. Expressway is built to connect all areas.

```js
"seed": "878463",
"terrain": ["plains", "forest", "snowy hills", "river", "beach"],
"centerCoordOfSource": [606, 310, -280],
"version": "1.20",
"road types": ["paved"],
"add-ons": "none(vanilla)"
```

#### Bandar

Located at central to east plains of the island. This is a Kuala Lumpur, Malaysia themed city with some iconic buildings in Malaysia. Also featuring Malaysian style roads (elevated highway, roundabout, complex one-way streets) and terrace houses.

{{< details "Documentation Details" >}}

| Build | Source |
| - | - |
| Petronas Twin Towers | Hand build from this [model](https://sketchfab.com/3d-models/petronas-towers-098e8f84b19d40ab91b51792482bcf48) and various pictures from the web |
| Merdeka pnb 118 | Use obj2sch from this [model](https://sketchfab.com/3d-models/pnb-118-1669baef4fa1408d958626ee24b6ef48) |
| Malaysia Terraced House | - |

{{< /details >}}

#### City

Located at south plains of the island. This is a well planned North America themed urban city with modern concepts like aesthetics, blocky urban, green, safe, walkable, cyclist friendly, public transport, low-high building landscape curves. Also, each street has different style. This is inspired by creation of a YouTuber, Alpine.

{{< details "Documentation Details" >}}

| Street | Name | Source |
| - | - | - |
| Townhouse Street | Soho House | Alpine1 [soho penthouse](https://youtu.be/7CK2x3HyHXI?si=8cw78-Ca2Orkvx1x) |
| Modern Street | Galleria - Showroom for arts, shaders, texture packs | Alpine1's video at [london](https://youtu.be/SQOlDp9txT4?si=icO2I2e8Co_v9CMe) |
| Modern Street | Starbucks | MC老玩家的一生, modified |
| NYC Street | NYC | [Pinterest1](https://www.pinterest.com/pin/2603712281850828/), [Pinterest2](https://www.pinterest.com/pin/8585055535931878/) |
| Port | Ships | 3D models from sketchfab: [Crane](https://skfb.ly/69zJo), [Cruise](https://skfb.ly/oG8xG), [Large Cargo](https://skfb.ly/oUXZK), [Small Cargo](https://skfb.ly/6W88o), [Yatch1](https://skfb.ly/oN9PU), [Yatch2](https://skfb.ly/6XFzD), [Sailboat](https://skfb.ly/MoEQ), [Fishing Boat](https://skfb.ly/pqVyE) |

{{< /details >}}

#### Gemilang

Located at the northern jungle of the island. This is a collection of traditional Malay-Austronesian architecture village.

{{< details "Documentation Details" >}}

| Build | Source |
| - | - |
| Istana Melaka | Hand build from this [model](https://sketchfab.com/3d-models/istana-kesultanan-melaka-19492b420bf64443877f89091db5cbc2) |
| Rumah Kampung I | Hand build from this [model](https://sketchfab.com/3d-models/house-of-malaysia-ee281bbc363b44d1a82eb17b788d1989) |
| Rumah Gadang | [model](https://sketchfab.com/3d-models/rumah-gadang-sumatra-barat-indonesia-be692baf8eb34cd99eb7b37ad531256c) |
| Rumah Traditional Terengganu | [model](https://sketchfab.com/3d-models/malaysia-rumah-tradisional-terengganu-0037c6c067e14786a3215ce63efe31a8) |

<!-- Malay-Indo architectual styles: elevated for safety, wood, roof for ventilation

| Name | Description | Region |
| - | - | - |
| Rumah Limas / Lipat Kajang | Flat roof surface, crossing edge | Modern malay building, istana melaka, south sumatra, jawa barat, malaya |
| Rumah Lancang / Lontik | Curved Roof | Riau, Jambi, Negeri Sembilan |
| Rumah Gadang | Curved sharp roof surface to the sky | Minangkabau (West Sumatra) |
| Rumah Perabung Lima | Connected house | Kelantan, Terengganu |
| Rumah Bumbung Panjang | Long roof | All |
| Rumah Iban & Kadasan | Long house | Sabah, Sarawak, Borneo |
| Rumah Ayer | Water house | All |
| Batak House (Bolon) | Very high and curved spanned horizontally roof | Batak (North Sumatra) |
| Javanese House | Very high and centered roof | Java |
| Tongkonan | High-saddle shape roof | Sulawesi | -->
<!-- [source](https://buildingconservation.blogspot.com/2007/08/lukisan-terukur-rumah-melayu.html) and wikipedia. -->

{{< /details >}}

#### Sapi

Spawn village of my legacy sapi world. This world started as a creative multiplayer building world. My training ground for wood house building from YouTube tutorial videos by Grian, JeraCraft, and others.

#### East City

Located at east side of the island.

{{< details "Documentation Details" >}}

| Build | Source |
| - | - |
| Dormitory | NCUE Dorm 10 |

{{< /details >}}

#### Coming soon

Taiwanese (concrete & modern), Japanese (suburban house), French(Paris), Italian(organic), Spanish(street), Spanish Colonial (mexican) street, Nordic

### Oriental Island

![south](images/minecraft/planning/south_island.png)

Located at the south of the main island. A east-asia themed island with various oriental style village around the island.

```js
"seed": "-1818114357538776435",
"terrain": ["snowy hills", "forest"],
"centerCoordOfSource": [448, 320, 320],
"version": "1.20",
"road types": ["grass", "paved"],
"add-ons": "none(vanilla)"
```

#### Nanyang

A port city on the east coast is build inspired by the Southeast Asia Nanyang style buildings.

### West Island

![west](images/minecraft/planning/west_island.png)

Located at west of main island. The shape of the island looks like the UK. It's an island of industrial, hanged structures at hills, Victorian and gregorian street house collections.

```js
"seed": "53285197",
"terrain": ["plains", "jungle", "snowy hills", "lush cave"],
"centerCoordOfSource": [192, 320, 704],
"version": "1.20",
"road types": ["grass", "paved"],
"add-ons": "none(vanilla)"
```

### North Island

![north](images/minecraft/planning/north_island.png)

Located at north of main island. European medieval and fantasy themed island, connected with minecart railway systems. Lush cave hidden in the underground of the island.

```js
"seed": "-156227665",
"terrain": ["dark oak forest", "snow plains", "lush cave"],
"centerCoordOfSource": [-704, 320, -768],
"version": "1.20",
"road types": ["grass"],
"add-ons": "none(vanilla)"
```

### Cherry Island

![cherry](images/minecraft/planning/cherry_island.png)

An small island of cherry blossom mountain surrounding a lake.

```js
"seed": "1691256543523180978",
"terrain": ["cherry blossom", "dark oak forest"],
"centerCoordOfSource": [12000, 310, -1500],
"version": "1.21",
"road types": [""],
"add-ons": "none(vanilla)"
```

### Pale Island

![pale](images/minecraft/planning/pale_island.png)

An island of large pale garden.

```js
"seed": "-1106759604738884840",
"terrain": ["pale garden", "tall birch forest","ancient city"],
"centerCoordOfSource": [-300, 310, 400],
"version": "1.21",
"road types": [""],
"add-ons": "none(vanilla)"
```

### Villager Island

![village](images/minecraft/planning/village_island.png)

An small island beside west island with woodland mansion and village.

```js
"seed": "-3420545464665791887",
"terrain": ["island"],
"centerCoordOfSource": [130, 310, 50],
"version": "1.21",
"road types": [""],
"add-ons": "none(vanilla)"
```

### Snow Island

![snow](images/minecraft/planning/snow_island.png)

Far northeast island of cold biomes.

```js
"seed": "29955740362394674",
"terrain": ["snowy plains", "snowy spruce jungle", "ice spikes", "icebergs"],
"centerCoordOfSource": [-1300, 310, 400],
"version": "1.21",
"road types": [""],
"add-ons": "none(vanilla)"
```

### East Island

![east](images/minecraft/planning/east_island.png)

Northeast island of warm biomes.

```js
"seed": "-1754216045272489466",
"terrain": ["desert". "mangrove", "badlands", "wooded badlands", "eroded badlands", "warm ocean", "savana"],
"centerCoordOfSource": [1300, 310, -2600],
"version": "1.21",
"road types": [""],
"add-ons": "none(vanilla)"
```
