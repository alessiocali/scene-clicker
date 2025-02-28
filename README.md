![](https://img.shields.io/badge/Foundry-v0.8.8-informational)
![GitHub All Releases](https://img.shields.io/github/downloads/jegasus/scene-clicker/total?label=Downloads+total)  
![Latest Release Download Count](https://img.shields.io/github/downloads/jegasus/scene-clicker/latest/module.zip)
![Forge Installs](https://img.shields.io/badge/dynamic/json?label=Forge%20Installs&query=package.installs&suffix=%25&url=https%3A%2F%2Fforge-vtt.com%2Fapi%2Fbazaar%2Fpackage%2Fscene-clicker&colorB=4aa94a)

# Scene Clicker
A [FoundryVTT](https://foundryvtt.com/) module that changes the behavior of left clicking on a Scene or a Scene Link. When this module is activated, left-clicking on a Scene or a Scene Link will "view" the Scene instead of rendering the Scene Config Sheet.

# Installation and setup
The Scene Clicker module requires you to install [ruipin's libWrapper library](https://github.com/ruipin/fvtt-lib-wrapper). 

Activating both modules in your world will override the left-click behavior on Scenes.

# Instructions
- Step 1: activate this module in your world 
- Step 2: in the Scenes Directory panel, in Journal Entries or on the Navigation menu, left-click on any of your scenes
- Step 3: bask in the glory of viewing the Scene instead of having the Scene Config Sheet pop up

<ins>**Additional options**</ins>: hold <kbd>Ctrl</kbd> to Activate the Scene or hold <kbd>Alt</kbd> to render the Config Sheet.

![Journal scaler in action](img/module_in_action.gif)

![Journal scaler in action with Journal links](img/module_in_action_2.gif)

# Changelog

## 0.0.10 - Released on 2021-08-01
Enormous thanks to [Alessio Calì](https://github.com/alessiocali) for making the required changes to update the Scene Clicker module to 0.8.x.

Removed the use of the `libWrapper` shim. Now, the full `libWrapper` library is required to run this module.

## 0.0.9 - Released on 2021-03-19
Added extra functionality: The hotkeys now work when clicking on the Scenes in the navigation bar too!

## 0.0.8 - Released on 2021-03-10
Added extra functionality: Use Ctrl+LeftClick to Activate Scene and Alt+LeftClick to Render the Scene Config Sheet.

## 0.0.7 - Released on 2021-01-10
Added support to clicks on Journal links. Special thanks to [ruipin](https://github.com/ruipin) for his help troubleshooting!!!!

## 0.0.6 - Released on 2020-12-25
Initial release. Merry Christmas, y'all <3

# Acknowledgements

## LoFD's Module Template
This module relied heavily on [The League of Foundry Developer's FoundryVTT Module Template](https://github.com/League-of-Foundry-Developers/FoundryVTT-Module-Template). This is a great resource to get started in developing cool stuff for FoundryVTT!

## ruipin's libWrapper
This module uses [ruipin's libWrapper library](https://github.com/ruipin/fvtt-lib-wrapper). Take a look at his stuff if you want to develop modules for FVTT that override its default behaviors.

## D20 Day Hackathon
This module was originally developed during the [D20 Day Hackathon](https://www.reddit.com/r/FoundryVTT/comments/k8ly5i/the_1st_annual_d20_day_hackathon/) in 2020. 

## Important note
A part of the module still needs to be re-written - specifically, the wrapper on the `SidebarDirectory.prototype._onClickEntityName` function. This will be deprecated in 0.9.x and needs to be updated to the `Document#documentName` property instead.
