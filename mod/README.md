# Overview

Have you found yourself in a diverse galaxy, full of worlds that would better off with a healthy ~~glassing~~ "terrestrial resurfacing" from orbit?  Those colorful skies are far too cheerful to allow for proper introspection on the dead - and how could they ever be home without comfortingly high levels are background radiation?  This mod is an expansion of ["Terraform" to Tomb World](https://steamcommunity.com/workshop/filedetails/?id=2625663437) that adds compatibility with [Planetary Diversity](https://steamcommunity.com/workshop/filedetails/?id=819148835) (and its submods).

Suggested by [NivMizzet Firemind](https://steamcommunity.com/profiles/76561198276935683).

# Changes

Adds terraforming links to change many any colonizable, non-artificial planet classes from Planetary Diversity (and its submods) into a tomb world (`pc_nuked`).

## What Can't I Nuke?

* As with the main mod, ecumenopolis planets cannot be converted (directly) to Tomb Worlds
* Planetary Diversity adds special habitable classes intended only for use as special graphical variations - this mod does not add terraform links, and neither does PD provide any to/from the "display only" planet classes
* Shrouded worlds - the Shroud is amused by your pitiful displays of material power
* Most unhabitable planet classes (Hothouses are able to be terraformed when the Terraforming Candidate modifier is present)
* All unique planet classes (Crystal, etc.) - PD does not allow terraforming these planet classes

## Compatibility

Built for Stellaris version 3.6 "Orion."  Not compatible with achievements.

Only adds new terraforming links, so it should not conflict with other mods that do not also add terraforming links from and to the same planet classes.  This submod adds compatibility for Planetary Diversity.

### Required Dependency Mods

* ["Terraform" to Tomb World](https://steamcommunity.com/workshop/filedetails/?id=2625663437) for the events that apply the "terraforming" graphics and framework code to make this mod work
* [Planetary Diversity](https://steamcommunity.com/workshop/filedetails/?id=819148835) to provide new planet classes - otherwise this mod does nothing

### Recommended Companion Mods

* [Planetary Diversity - Unique Worlds](https://steamcommunity.com/workshop/filedetails/?id=1740165239)
* [Planetary Diversity - More Arcologies](https://steamcommunity.com/workshop/filedetails/?id=1732447147)
* [Planetary Diversity - Exotic Worlds](https://steamcommunity.com/workshop/filedetails/?id=1732437279)
* [Planetary Diversity - Planetary Habitats](https://steamcommunity.com/workshop/filedetails/?id=1878751971)
* [Planetary Diversity - Shroud Worlds](https://steamcommunity.com/workshop/filedetails/?id=1960179456)

### Not Included in "Subtle Polish"

This mod is intentionally not included in my modpack [Subtle Polish: A Collection of Fixes and Enhancements](https://steamcommunity.com/workshop/filedetails/?id=2522974089) because it a compatibility patch for a specific, additional mod.  Will otherwise function alongside Subtle Polish when combined with Planetary Diversity.

## Known Issues

Overrides four scripted triggers and one scripted effect from "'Terraform' to Tomb World" in order to add Planetary Diversity support.  Expect to see five entries in the error.log file similar to these:

```
[00:53:03][game_singleobjectdatabase.h:165]: Object with key: eligible_pc_nuked_terraform_habitable already exists, using the one at  file: common/scripted_triggers/02_terraform_to_pc_nuked_pd_scripted_trigger_overrides.txt line: 3
[00:53:03][game_singleobjectdatabase.h:165]: Object with key: eligible_pc_nuked_terraform_hostile already exists, using the one at  file: common/scripted_triggers/02_terraform_to_pc_nuked_pd_scripted_trigger_overrides.txt line: 113
[00:53:03][game_singleobjectdatabase.h:165]: Object with key: eligible_pc_nuked_terraform_unhabitable already exists, using the one at  file: common/scripted_triggers/02_terraform_to_pc_nuked_pd_scripted_trigger_overrides.txt line: 134
[00:53:03][game_singleobjectdatabase.h:165]: Object with key: is_nuked_species already exists, using the one at  file: common/scripted_triggers/02_terraform_to_pc_nuked_pd_scripted_trigger_overrides.txt line: 186
[00:53:03][game_singleobjectdatabase.h:165]: Object with key: post_terraform_to_pc_nuked already exists, using the one at  file: common/scripted_effects/02_terraform_to_pc_nuked_pd_scripted_effect_overrides.txt line: 3
```

## Changelog

* 1.0.0 Initial version
* 2.0.0 Update for Stellaris version 3.4 "Cepheus" - use memory optimization feature for effects and triggers
* 2.1.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax")
    * Account for new radiotrophic variants
    * Support changes to terraforming frozen worlds (you can still nuke them if they have the `frozen_terraforming_candidate` modifier)
    * Improve check for "is a species "'nuked?'"
    * Add terraform links for Planetary Diversity classes that are new (tidally-locked, super-habitable, and cave variants, plus five rare worlds)

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/terraform_to_pc_nuked_pd)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.