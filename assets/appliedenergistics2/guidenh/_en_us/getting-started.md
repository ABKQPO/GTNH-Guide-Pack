---
navigation:
  title: Getting Started
  position: 10
  parent: index.md
---

# Quick Start

# Simple Storage Network
To get you easily started with AE2, let's first build a simple storage network to achieve AE2's basic function: storage.

## Prerequisites
Applied Energistics 2 is actually alien technology. You can find [Meteorites](./ae2-mechanics/meteorites.md) scattered across the world. In their cores, there might be a <ItemLink id="appliedenergistics2:tile.BlockSkyChest" showIcon="left"/>. Inside these chests, you have a chance to find the core items of AE2: <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:13" showIcon="left"/>, <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:14" showIcon="left"/>, <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:15" showIcon="left"/>, and <ItemLink id="appliedenergistics2:item.ItemMultiMaterial:19" showIcon="left"/>. You need these to craft AE2 components and blocks. Furthermore, in GTNH, AE2 has been integrated into GregTech; you will need to reach the EV tier and obtain Titanium before you can manufacture an AE system.

## Materials
Once you have reached the technological level required to build an AE system, you will also need the following materials:
- <ItemImage id="gregtech:gt.blockores2:516" label="right"/>
  - We need to obtain <ItemImage id="gregtech:gt.metaitem.01:2516"  label="right"/> and <ItemImage id="gregtech:gt.metaitem.01:8516" label="right"/> from this, which are important raw materials for crafting AE items and blocks.
- <ItemImage id="gregtech:gt.blockores2:28" label="right"/>
  - Many AE blocks require <ItemImage id="gregtech:gt.metaitem.01:17028" label="right" /> to craft.
- Other basic materials such as <ItemImage id="minecraft:redstone" label="right" />, <ItemImage id="minecraft:diamond" label="right"/>, and <ItemImage id="dreamcraft:CircuitHV"  label="right"/>. You have certainly encountered these materials on your way to the EV tier, so they will not be elaborated on here.

## Construction
Once everything is ready, let's build the simple storage network below. You need to set up the following scene.

<GameScene zoom="5" interactive={true} width="400" height="300">
  <ImportStructure src="assets/structures/getting-started.snbt" />
  <IsometricCamera yaw="200" pitch="30" />
  <BlockAnnotation pos="5 0 0" color="#e5e90c" alwaysOnTop={true}>
  <Color color="#e5e90c">This is a Debug Generator placed for demonstration purposes and cannot be obtained in Survival mode. For normal use, please connect to your power grid.</Color>
  </BlockAnnotation>
</GameScene>

The AE system in the scene relies on the GT power grid on the left for power. This AE system implements basic item storage functionality:
- The <ItemLink id="appliedenergistics2:tile.BlockController" showIcon="left"/> provides [Channels](./ae2-mechanics/channels.md) to the entire network.
- <ItemLink id="appliedenergistics2:item.ItemMultiPart:36" showIcon="left"/> connect all components in the network.
- An <ItemLink id="appliedenergistics2:item.ItemBasicStorageCell.1k" showicon="left"/> is placed inside the <ItemLink id="appliedenergistics2:tile.BlockDrive" showIcon="left"/> to provide storage space.
- An <ItemLink id="appliedenergistics2:item.ItemMultiPart:220" showIcon="left"/> is placed against a chest to integrate the chest's storage space into the AE network.
- An <ItemLink id="appliedenergistics2:item.ItemMultiPart:380" showIcon="left"/> provides a channel for players to interact with the internal space of the AE network.

Now you can right-click the terminal to open the AE storage network, inserting or extracting items from the terminal just like you would normally use a chest. Items manually placed into the chest will also be displayed in the AE terminal. At this point, you have successfully built an AE storage network, but this is only the tip of the iceberg for AE networks. Please continue exploring this guide for more content.

[Items and Blocks](items-blocks-index.md)

[AE2 Mechanics](ae2-mechanics-index.md)

[Tips and Practical Examples](tricks-example.md)

## Matter Energy Tech: ME Networks and Storage

### What is ME Storage?

Its pronounced Emm-Eee, and stands for Matter Energy.

Matter Energy is the main component of Applied Energistics 2, it's like a mad scientist version of a Multi-Block chest,
and it can revolutionize your storage situation. ME is extremely different than other storage systems in Minecraft, and
it might take a little out of the box thinking to get used to; but once you get started vast amounts of storage in tiny
space, and multiple access terminals are just the tip of the iceberg of what becomes possible.

### What do I need to know to get started?

First, ME Stores items inside of other items, called [Storage cells](items-blocks-machines/storage_cells.md); there are 5 tiers with ever increasing amounts of
storage. In order to use a Storage Cell it must be placed inside either an <ItemLink id="me_chest" />,
or an <ItemLink id="drive" />.

The <ItemLink id="me_chest" /> shows you the contents of the Cell as soon as its placed inside, and you
can add and remove items from it as if it were a <ItemLink id="minecraft:chest" />, with the exception that the items are
actually stored in the Storage cells, and not the <ItemLink id="me_chest" /> itself.

The <ItemLink id="me_chest" /> is quite situational and limited in utility. To really
take advantage of AE2, you need to set up an [ME Network](ae2-mechanics/me-network-connections.md).

## Your Very First ME System

Now that you have all of the basic materials and machines for Applied Energistics 2, you can make your first ME (Matter Energy) system. This will be a very basic one, no autocrafting, no logistics, just nice, simple, searchable storage.

<GameScene zoom="6" interactive={true}>
<ImportStructure src="assets/assemblies/tiny_me_system.snbt" />

</GameScene>

*   Your ingredients list:
    * 1x <ItemLink id="drive" />
    * 1x <ItemLink id="terminal" /> or <ItemLink id="crafting_terminal" />
    * 1x <ItemLink id="energy_acceptor" />
    * A few [cables](items-blocks-machines/cables.md), either glass, covered, or smart, but not dense
    * A few [storage cells](items-blocks-machines/storage_cells.md), recommended of the 4k variety for a good mix of
    capacity and types (it would be more efficient to [partition](items-blocks-machines/cell_workbench.md) a mix of 4k and 1k but that's a complexity we won't go into now)
---
1.  Place the drive down.
2.  The energy acceptor (and several other AE2 [devices](ae2-mechanics/devices.md)) comes in 2 modes, cube and flat. They can be switched between in a crafting grid. If your energy acceptor is a cube, place it down next to the drive. If it's a flat square, place a cable on the drive and place the acceptor on that.
3.  Run energy into the energy acceptor with a cable/pipe/conduit from your favorite energy-generation mod.
4.  Place a cable on top of the drive (or otherwise at eye level) and place your terminal or crafting terminal on it.
5.  Put your storage cells into the drive
6.  Profit
7.  Fiddle with the terminal's settings
8.  Bask in your ultimate power and ability
9.  Realize that this network is, in the grand scheme, rather small

### Expanding your Network

So you have some basic storage, and access to that storage, it's a good start, but you'll likely be looking to maybe
automate some processing.

A great example of this is to place a <ItemLink id="export_bus" /> on the top of a furnace to
dump in ores, and a <ItemLink id="import_bus" />
on the bottom of the furnace to extract furnaced ores.

The <ItemLink id="export_bus" /> lets you export items from the network, into the attached
inventory, while the <ItemLink id="import_bus" /> imports items from the attached inventory into
the network.

### Overcoming Limits

At this point you probably getting close to 8 or so [devices](ae2-mechanics/devices.md), once you hit 9 devices you'll have to start
managing [channels](ae2-mechanics/channels.md). Many devices but not all, require a channel to
function.

By default a network can support 8 channels, once you break this limit, you'll have to add
an <ItemLink id="controller" /> to your network. this allows you to expand your network greatly.
[Smart cables](items-blocks-machines/cables.md) will allow you to see how channels are routed through your network. Use them extensively when starting out to learn how channels act, or if you have a lot of redstone and glowstone.
