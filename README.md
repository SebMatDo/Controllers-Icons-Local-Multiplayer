# THIS ADDON IS NOW DEPRECATED, as now the original addon fixed this issue with a better approach PLEASE USE THE ORIGINAL ONE, 

This is based on https://github.com/rsubtil/controller_icons/?tab=readme-ov-file for Godot 4.x version
This addon let you to show icons of the current devices that players are using (including keyboard) or in case that it doesn't recognize the controller brand/name it will auto fallback to xbox360 icons.
You could run the demo showcase to see how it is working.

Created and used for my game Fat Cat Fest  https://store.steampowered.com/app/3259080/The_Fat_Cat_Fest/

# Features
- Show keyboard or controller icons to each player based on their device. This allow for automatic icon glyphs on local multiplayer
- Handles generic controller paths to support many different button icons
- Ships with default assets for keyboard and mouse, and most popular controllers

![image](https://github.com/user-attachments/assets/ec33e973-72a3-47b4-8f2e-27ee23c94024)
![image](https://github.com/user-attachments/assets/760e9cdf-1acc-458a-92cc-cfaa1e62d731)

# Changes made
- You can select the player in the icon texture
- You can call ControllerIcons.reload.emit() after remapping or changing devices to reload / change the icons in runtime.
- You can and should call to update the devices of the players, up to 8 players. ControllerIcons.update_player_device(ControllerIcons.PlayerDevices.Player1, device)
- This addon doesn't automatic change the icon when you use keyboard/controller, you must choose one to show.

# Installation
This is the Godot 4.x version.
The minimum Godot version is 4.1.2 (stable).
Download this repository and copy the addons folder to your project root directory.
Then activate Controller Icons Local Multiplayer in your project plugins.

# Tutorial of the base of the addon
check the https://github.com/rsubtil/controller_icons/?tab=readme-ov-file tutorial.

# Credits
Thanks @rsubtil for the base of this addon, most part of this addon is from him.

# License
The addon is licensed under the MIT license. Full details at LICENSE.
The controller assets are Xelu's FREE Controllers & Keyboard PROMPTS, made by Nicolae (XELU) Berbece and under Creative Commons 0 (CC0). Some extra icons were created and contributed to this addon, also on the same CC0 license:
@TacticalLaptopBag: Apostrophe, backtick, comma, equals, forward slash and period keys.
The icon was designed by @adambelis (#5) and is under Create Commons 0 (CC0). It uses the Godot's logo which is under Creative Commons Attribution 4.0 International License (CC-BY-4.0 International)

# Known issues
- In the editor to see the change of player in the panel of select path (the one that let you watch all the input bindings) you need to change the player, then select another node, then you could select the node that you changed and see the bindings with the selected player (I didn't know how to reload that with the proper parameter of the IconTexture)
- Error at loadinng the plugin without enabling it
- Nothing is shown if you select controller mode with an input path that doesn't has an controller input mapped in the project settings (in-game you can reload, this is not possible in the editor, so you should have default inputs of controllers)
