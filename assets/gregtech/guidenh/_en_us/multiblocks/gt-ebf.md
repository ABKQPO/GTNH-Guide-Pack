---
item_ids:
    gregtech:gt.blockmachines:1000
navigation:
    title: Electric Blast Furnace
    parent: index.md
    icon: gregtech:gt.blockmachines:1000
---

# Electric Blast Furnace

<GameScene interactive={true} wrap="square" align="right" width="380" height="300" >
  <ImportStructure src="/assets/structures/ponders/multiblocks/ebf_ponder.snbt" />
  <ImportPonder src="/assets/structures/ponders/multiblocks/ebf_ponder.json" />
</GameScene>

## <ItemImage id="gregtech:gt.blockmachines:1000"/> Electric Blast Furnace

```filetree
|-- **Source**:         [GregTech5u](https://github.com/GTNewHorizons/GT5-Unofficial/blob/master/src/main/java/gregtech/common/tileentities/machines/multi/MTEElectricBlastFurnace.java)
|-- **Machine Type**:   Blast Furnace
|-- **Tier**:           [LV]()
\-- **Details**
    |-- **Size**:                   3x3x4
    |-- **[Energy Hatches]()**:     Standard
    |-- **[Overclocks]()**:         Imperfect
    \-- **[Pollution]()**:          400 gibbl/s
```

The <ItemImage id="gregtech:gt.blockmachines:1000" /> **Electric Blast Furnace** (**EBF**) is an [LV]()
tier [multiblock](/multiblocks/index.md) for smelting dusts into ingots at a higher heat than standard furnaces. 

The EBF is a direct upgrade from the [Bricked Blast Furnace]() because it runs off electricity instead of burnable fuels 
and can process higher tier materials. 

The [heating coils]() in the structure determine the heat capacity of the machine and the energy hatch(es) determine the 
voltage. Upgrade both to unlock new recipes and [overclock]() the machine. 

The EBF follows standard multiblock behaviors such as releasing pollution from a muffler hatch, 
occasionally requiring [maintenance](), and voiding ingredients on power fail. 
Items and fluids are inserted/extracted through buses and hatches, respectively.

<RecipesFor id="gregtech:gt.blockmachines:1000"/>

# Construction
The EBF is built with Heat Proof Machine Casings on the top and bottom layers and heating coils in the middle two layers. 
The heating coils determine the heat capacity of the machine and must all be the same tier for the structure to form.

Buses/hatches may only replace the casings on the bottom layer, except for the muffler hatch which is restricted to the top center casing. 
Another exception is the output hatch which collects fluids while on the bottom layer and gases while on the top layer. 

The amount of gas recovered depends on the tier of the muffler hatch. 

The EBF runs at the voltage tier of the energy hatch, but can overclock to the next voltage tier with two of them. 

Use the [Multiblock Structure Hologram Projector]() to visualize/build the structure with subchannel "coil" to specify the tier of the heating coils. 

| Requires                                                                                    |
|:--------------------------------------------------------------------------------------------|
| 1 <ItemImage id="gregtech:gt.blockmachines:1000" /> **Electric Blast Furnace** (controller) |
| 16 <ItemImage id="gregtech:gt.blockcasings5" /> **Heating Coil**[^one]                      |
| 0-15 <ItemImage id="gregtech:gt.blockcasings:11" /> **Heat Proof Machine Casing**           |
| 1+ <ItemImage id="gregtech:gt.blockmachines:41" /> **Energy Hatch** (any bottom casing)     |
| 1 <ItemImage id="gregtech:gt.blockmachines:90" /> **Maintenance Hatch** (any bottom casing) |
| 1 <ItemImage id="gregtech:gt.blockmachines:91" /> **Muffler Hatch** (top center casing)     |
| 0+ <ItemImage id="gregtech:gt.blockmachines:71" /> **Input Bus** (any bottom casing)        |
| 0+ <ItemImage id="gregtech:gt.blockmachines:51" /> **Input Hatch** (any bottom casing)      |
| 0+ <ItemImage id="gregtech:gt.blockmachines:81" /> **Output Bus** (any bottom casing)       |
| 0+ <ItemImage id="gregtech:gt.blockmachines:61" /> **Output Hatch** (any top/bottom casing) |
[^one]: This is a **TIERED** component.

> [!WARNING]
> Multi-amp and laser [energy hatches]() are not supported.

## Wallsharing

EBFs may [wallshare]() each of their sides to save on casings, heating coils, and buses/hatches. 
Overlapping EBFs side-by-side is the most effective and highly recommended because it saves a significant amount of 
heating coils and reduces the cost of additional EBFs.

For example, a quad-shared EBF requires only 42 heating coils to build instead of the full 64. 
The only downside is the difficulty in upgrading heating coils because they must all be the same tier for the structure(s) to form. 

Sharing a maintenance hatch, output bus, and input hatch is also quite useful, but do NOT share energy hatches because the EBF 
frequently needs to be overclocked to a higher voltage tier which uses the maximum 4A from two energy hatches. Splitting that between two machines is simply not possible and causes one to power fail. 

> [!CAUTION]
> There are a few potential hazards for GregTech multiblocks that could cause them to power fail or even explode. 
> * Do not expose the EBF to the rain. 
> * Do not block the muffler hatch with any sort of block, cable, or pipe. 
> * Do not exceed the voltage tier of the energy hatches. 
> * Provide consistent power during the entire recipe. 
> * Ensure there is space for any outputs if void protection is enabled.

# Usage
The EBF is finally ready for use once the structure is formed and all maintenance issues are repaired. However, there are no LV recipes despite the player only having access to LV energy hatches; processing steel and aluminium requires at least MV power. The solution is to build two energy hatches into the structure to overclock the machine to the next voltage tier. Energy hatches normally only pull 1A of power but they are capable of pulling up to 2A for scenarios such as this. This means two energy hatches can pull 4A of power, or the equivalent of 1A of the next voltage tier.

Supplying a continuous 4A of power requires at least four singleblock steam turbines nearby. The recipes for steel and aluminium only consume 120 EU/t so there can be some cable loss but not very much. The following are the two methods for meeting these power requirements and running the EBF. These both assume that the player is NOT using superconductor wires which have zero cable loss regardless of the amps or distance. 
