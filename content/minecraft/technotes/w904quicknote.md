---
title: "Quicknote"
description: ""
summary: ""
date: 2024-10-08T19:53:05+08:00
lastmod: 2024-10-08T19:53:05+08:00
draft: false
weight: 904
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

### My mod shortcuts notes

| Mod | Hotkey | Shortcut |
| - | - | - |
| Iris | `O` | Open shader menu |
| Xaero's Map | `M` | Open Map |
| WorldEdit | Wooden Axe | `left click` choose pos1, `right click` choose pos2 |
| WorldEdit | Compass | `left click` teleport to crosshair, `right click` pass through wall |
| Litematica | Stick | `ctrl + scroll` choose type, `alt + scroll` to move schematic |
| Litematica | `N` | Open Menu |
| Litematica | `N + P` | Execute (Paste) |
| Litematica | `N + T` | Toggle selection |
| Axiom | `Right Shift` | Open UI menu |
| Axiom | `B` | Utilities |

### Minecraft Quick Note

```js {title="Code"}
const color = {0: "White", 1: "Orange", 2: "Magenta", 3: "Light Blue", 4: "Yellow", 5: "Lime", 6: "Pink", 7: "Dark Grey", 8: "Light Grey", 9: "Cyan", 10: "Purple", 11: "Blue", 12: "Brown", 13: "Green", 14: "Red", 15: "Black"}

const stone = { 0: "Stone", 1: "Granite", 2: "P. Granite", 3: "Diorite", 4: "P. Granite", 5: "Andesite", 6: "P. Andesite" }

const planks = { 0: "Planks", 1: "Spruce", 2: "Birch", 3: "Jungle", 4: "Acacia", 5: "Dark Oak"}

const stone2 = { 0: "Sandstone", 1: "chiseles", 2: "cut", 3: "smooth" }
```

```txt {title="Quick Commands"}
# Syntax
/fill execute at NutNut17 run fill ~2 -1 ~2 ~-2 ~-1 ~-2

# Circle Generator
[spin] execute as @e[type=armor_stand] at @s run tp @s ~~~ ~1.5 ~; 1.5:Angle of rotation
[setblock] execute at @e[type=minectaft:armor_stand] run setblock ^^^10 glass; 10:radius
```

### WorldEdit

#### Basic

| Command | Use |
| - | - |
| `//wand` | Get a tool, left-click(pos1), right-click(pos2) |
| `//pos1`, `//pos2` | Select stand position |
| `//hpos1`, `//hpos2` | Select on crosshair |
| `//drawsel` | Display selected region |
| `//undo`, `//redo` | - |
| `//set <block>` | Fill a region with block |
| `//set 50%air,50%water` | Fill region with different block and proportion |
| `//replace <block1> <block2>` | Replace block1 with block2. In default, replace all except air |
| `//copy`, `//paste` | The block you paste is based on the location you copy |
| `//move <n> <attr>` | Move the selected region n block to the direction user face. Put '-a' as attr to avoid air replacing existing block |
| `//stack` | Stack to facing direction |
| `//rotate <y-axis angle> <x-axis angle> <z-axis angle>`, `//flip` | the center will be the position you stand when the region you copy |
| `//shift`, `//expand`, `//contract` | Operations |
| `//expand vert` | Expand to vertical limit |
| `//inset`, `//outset` | Contract or expand in all dimensions |
| `//trim` | Trim the excessive air blocks |
| `/asc`, `/desc`, `ceil`, `thru`, `j` | Navigation |
| `//line` | Draw a line |
| `//center` | Set block on the center |
| `//setbiome <biome>` | Set biome |
| `//fill <pattern> <radius> [depth]` | Fill a region with block |
| `//fillr <pattern> <radius> [depth]` | Fill a hole recursively |
| `//drain`, `/flood`, `/fixlava`, `/fixwater` | Liquid operations |
| `/butcher`, `/remove` | Remove mobs and entities |

#### Selection Modes

| Modes | Description |
| - | - |
| `//sel cuboid` | Default selection |
| `//sel extend` | Extend cuboid on every right click |
| `//sel poly` | Select first point by left-clicking, then select subsequent points by right-clicking |
| `//sel ellipsoid` | Select first point by left-clicking, then extend by right-clicking |
| `//sel convex` | Select first point by left-clicking, then extend by right-clicking. The selection is a convex hull encompassing all your selected points |

#### Brush and Tool

| Command | Use |
| - | - |
| `//brush <shape> <block:block to be paste> <radius:max=6>` | Add the brush effect to the tool user holding. Shape: sphere, cylinder |
| `//brush clipboard` -> `/gmask` | The copied item in clipboard is binded to brush right click using the brushed tool to paste the item |
| `//brush smooth <radius> <block>` | Apply smoothing effect on the brush |
| `//brush clipboard` | Copy clipboard to brush |
| `//tool unbind` | Remove the brush effect |
| `//mask <block1,block2,...>` | Brush only works on block1, block2, ... |
| `//mask` | Clear the mask |
| `//range` | Set the brush range |
| `/superpickaxe recursive` | Enable recursive destroy of same block |

#### Shape

| Command | Use |
| - | - |
| `//sphere <block> <radius>` | Make a sphere from your location |
| `//hollow` | Empty cuboid |
| `//cyl <block> <radius> <height>` | Make a cylinder from your location |
| `//hpyramid` | Hollow pyramid |
| `//wall` | Make a cuboid wall |
| `//overlay` | Set a block on top of blocks in the region |
| `//gen` | Generate a shape according to a formula |

**Tips on making a mountain**

1. Brush a tool with sphere and paint sand by masking air
2. Replace all sand with dirt
3. Change dirt to stone then add a layer of sand for grass

- Left click holding a compass to teleport and right click to pass through wall