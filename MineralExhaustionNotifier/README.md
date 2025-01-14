# DSP Plugins by AleksLT

## How to Install :

First Install Bepinex in your game
folder : https://bepinex.github.io/bepinex_docs/master/articles/user_guide/installation/index.html?tabs=tabid-win

Then Download the latest DLL of the mod : https://github.com/alekslt/DSPPlugins_ALT/releases

And add it to a new subfolder in bepinex plugins folder under the steam game folder : %steamapps\common%\Dyson Sphere Program\BepInEx\plugins\DSPPlugins_ALT

Launch the game and you should be all set !

After launching one time there will be a config file you can edit in %steamapps\common%\Dyson Sphere Program\BepInEx\net.toppe.bepinex.dsp.veinexhaustion.cfg

## How to use the Mineral Exhaustion Notifier mod ?

This mod gathers information on vein miners and logistic stations and present this information in a window allowing you to group by planet, resource and power network.

You can also filter what is shown by several filters to drill down to what you want to know. Mining rate, logistic station - item stock, ++.

The plugin will periodically check the miners for an alarm (Low Power, Low Production Yield), and/or if the remaining mineral they can mine is low or none.

If a miner is detected with this condition the toggle button (M) on lower right will change colour to red. To open the window press this button, or the bound quick key.

#### Quick Key map (configurable) : 

* ALT-I : Toggle Mineral Vein Information Window

## Screenshots

![Notification Box](https://raw.githubusercontent.com/alekslt/DSPPlugins_ALT/master/MineralExhaustionNotifier/Screenshots/InfoWindow.PNG)

![Full screen example image](https://raw.githubusercontent.com/alekslt/DSPPlugins_ALT/master/MineralExhaustionNotifier/Screenshots/FullGame.PNG)

## Changes in last release

### MineralExhaustionNotifier v0.5.2

* As some had grown used to the smaller window size with high resolution/pixel densities the scaling code is reworked to base itself on the games UI Layout Reference Height adjustment.
* If you are not happy with the size that the UI Layout Reference Height adjustment gives you there are config options that allow you to override the size. (Larger value = smaller window)
* In game window scale adjustment through - 1 + buttons on the window title bar.
* Fixed sorting for Logistic Stations - Resource. Now sorts on Resource Name, not the internal id. :)

### MineralExhaustionNotifier v0.5.1

* User customizable button placement
* Scaling code to give a consistent UI size independent of resolusion. (Thanks to yushiro for PR)
* Disabled initial pop-up, if alarm situation, for now as I personally didn't find this feature useful. Will bring it back after user customizable triggers are implemented.

### MineralExhaustionNotifier v0.5

* Added information on logistic stations and their items as well
* Filtering options. Filters are logically AND between the filters, and OR for the filter-local. Meaning you can do queries like: Stellar Stations AND Item % below 50%, AND Supply Remote.
* Show information from the data source ( Vein Miners or Logistic Stations) broken down into different groups. Planet style as it was, or Resource based to get a better understanding of everything related to titanium.
* Keybinding is now changed! You need to press an ALT-key before the user bindable key (default I)


## Verified working with game versions

* Dyson Sphere Project 0.6.16.5780
* Dyson Sphere Project 0.6.16.5759
* Dyson Sphere Project 0.6.15.5706
* Dyson Sphere Project 0.6.15.5686

## Acknowledgements

* Readme structure heavily inspired/copied from https://raw.githubusercontent.com/Touhma/DSP_Plugins
* Thanks to DSP Modding Discord
* UnityRunTimeEditor for the stop mouse events from propagating through window
* xiaoye97 for their LDBTool source that allowed me to understand enough GUI in the game to make my own
* ragzilla for DSP_MinerOverride giving me a nice place to look for mining-related classes
* Forked for poking me to create the Mineral Exhaustion notification plugin.
* yushiro for auto scaling code to better support high resolution displays.
