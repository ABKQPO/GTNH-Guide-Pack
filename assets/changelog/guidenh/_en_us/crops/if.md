---
navigation:
  title: Industrial Farm
  parent: crops.md
  icon: gregtech:gt.blockmachines:28055
categories:
    - crops
author: Skorched
date: 2026-05-20
---

# Industrial Farm
At a certain point in the game, your little old crop managers start struggling if you're really trying to push them to their limits. CropsNH comes with its own solution, the <Color id="GREEN">Industrial Farm</Color>

<GameScene wrap="square">
  <ImportStructureLib controller="gregtech:gt.blockmachines:28055" />
</GameScene>
The <Color id="GREEN">Industrial Farm</Color> is a customisable multiblock solution to your farming needs. It has a length from 3-14 depending on the tier it is built in, and allows lots of configuration depending on your specific needs.

The general form of the structure is set on both sides, with the "customisable" segment lying in the middle. Making the structure in MV means you can only have 1 "slice" in the centre, allowing for 3 seed beds, and 1 <Color id="RED">Upgrade Module</Color>. You unlock 1 extra slice per tier of energy hatch.

The Seed Beds, glass, and upgrade units are all <Color id="RED">TIERED</Color>, so take care to match them or you will run into problems.

## Modes
The <Color id="GREEN">Industrial Farm</Color> comes with 3 modes:
<Color id="RED">Input</Color> - Allows the entry of seeds and sub-soil blocks
<Color id="BLUE">Output</Color> - Ejects the seeds and sub-soil blocks stored in the machine
<Color id="GREEN">Farm</Color> - Actively farms the seeds and outputs the products to output buses

When in <Color id="GREEN">Farm</Color> mode, the multi runs on a fixed 5 second cycle regardless of tier or length. At the beginning of each cycle, water is consumed from the input hatch, and fertilizer if present and a fertilization unit is present. The amount consumed depends on the total capacity of the machine.

The farm simulates the growth of crops inside and scales the average result. It uses all the same equations as real world crop counterparts, aside from hydration and sky bonuses which are automatically maxed.

## Upgrade Units
The farm comes with a set of upgrade units which replace the top block in each slice of the machine:
- <Color id="GREEN">Advanced Harvesting Unit (MV+)</Color> - Increases drop amounts by 20% and consumption by 50% per unit. Limited to 2 per structure
- <Color id="RED">Fertilization Unit (MV+)</Color> - Requires the farm to always consume fertilizer at the beginning of each cycle to boost production. Boosts growth speed by 150%, output drops by 50%, and power consumption by 50%. Be careful - if you run out of fertilizer, it will stop completely. Limited to 1 per structure
- <Color id="BLUE">Environmental Enhancement Unit (MV+)</Color> - Unlocks an environmental module slot in the controller GUI, and increases consumption by 50%. These modules change the simulated temperature and/or biome inside the machine to provide more ideal growing conditions for specific crops. Limited to 2 per structure
- <Color color="#FF00FF">Growth Acceleration Unit (MV+)</Color> - Increases the growth speed by 100% and power consumption by 125% per unit. This unit is incompatible with the <Color color="#ffff00">Overclocked Growth Acceleration Unit</Color>. No limits.
- <Color color="#ffff00">Overclocked Growth Acceleration Unit (ZPM+)</Color> - Unlocks the use of <Color id="GREEN">Multi-Amp Energy Hatches</Color> and allows the farm to be overclocked with enough power. Limited to 1 per structure
