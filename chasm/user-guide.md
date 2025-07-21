# User Guide

Chasm is a diffusion / delay plugin with built-in controls and utilities to help you in your production. This guide covers the usage, preset manager and explains what each parameter controls, alongside some info about using the plugin and how to use it best.

## Using Chasm

Chasm is a versatile effect, containing a bunch of different things for you to work with, mess around with and use in your music. Some of the main components of this include:

- The main blur/delay effect
- Multiple filters for tweaking the sound
- Stereo Enhancement
- Haas Effect
- Built-in MakeItLoud

To use Chasm, first download the installer from your DirektDSP account, run it and scan for plugins in your DAW.
Next you need to authenticate. You can follow the UI in the plugin to do this.
Finally, you can start using Chasm.

On MacOS, if you run into issues opening the .pkg file, please try the following:

- Right click the .pkg and select open (you will get an error, do not delete the file)
- Open Privacy & Security settings, scroll down and select 'Open Anyways' beside the .pkg
- Use fingerprint or password to authorize
- Install as normal

Remember, Chasm is an effect plugin, not a instrument. In some DAWs like FL Studio, you will not be able to open it like an instrument.

## What the components do

### Delay Knob

The delay knob controls the amount of time the plugin will blur / delay your sound for.
This is based on a series of allpass filters, so by turning it down you get tighter blurs. Turning it up will result in longer, more noticable delays in your signal.

### Character Knob

The character knob controls the feedback of the allpass filters used in the main effect. Lower values reduce the amount of blur / delay. Values over 1 increate the metallic sound / resonance caused by the filters.

### Brightness Knob

This controls a high shelf filter applied to your audio after it is processed by the delay effect. This can help bring back the high end naturally lost by using multiple allpass filters.

### Width Knob

The width knob acts as a stereo enhancer, allowing you to boost the existing side information of the audio you send in. It is applied after the delay effect so will work a little even if the input audio was mono / had quiet side information.

### Haas Knob

The haas knob controls the time for the built-in haas effect. At 0 it behaves as if it is off. This effect is applied before the width knob's stereo enhancer, meaning you can really push your stereo if you want to!

### Low / High Cut Knobs

These knobs control low and high cut filters for the output wet audio. They can be used to clean up low end from sounds that might sound rumbly or interfere with themselves if the mix isn't 100%

### Input / Output Knobs

These control the input and output gain of the plugin.

### Mix Knob

Controls the wet/dry mix of the plugin. Values other than 100% have the chance to cause interference and phasing, which can sound really cool and emphasize the metallic sound of the plugin. Mess around with it!

## MakeItLoud Integration

The MakeItLoud implementation allows you to make your sound even louder and fuller without having to worry about clipping on your tracks. The implementation contains 2 identical compressors with a waveshaper gain inbetween, controlled by the mode dropdown.

This is disabled by default and can be enabled by selecting a mode from the mode dropdown

### Mode Dropdown

This controls the mode for the internal MakeItLoud implementation. The modes get increasingly louder as you go through them.

### Boost Knob

The boost knob controls the gain for the internal MakeItLoud implementation. This is the gain applied between both compressors in MakeItLoud, adding harmonics to your audio.

## Preset Manager

Chasm contains a unique, category-based preset manager.

This allows you to group all your favourite presets into categories you can make and edit in the plugin. No file explorer, no searching for folders. It just works.

### Making Categories

Click the large preset button and click 'Create New Category...'
Enter a name for your new category and press enter.
Your category has been made but won't show up immediately. We need to add presets to it.

### Saving Presets

To save a state you like into a preset, click the plus icon beside the preset selection menu.
Choose a category to save it to. You can also just save it to 'Default' if you don't want to put it in a category.

Type in a name you wish to save the preset as in your OS's file browser.
NOTE: You don't need to navigate into the category folder every time, Chasm just figures that bit out for you!

Optionally, you can save an artist name for the preset for a little bit of credit.
In Version 1.0 this isn't displayed but it allows us to implement it down the line.
Click save to finally save your preset

### Deleting Presets

Select the preset you want to delete and open it.
Click the X button on the right
Click 'Delete' to delete the preset

### Filesystem Layout

All your presets and categories are saved on your computer to the following locations:

| Operating System | Preset Location |
|------------------|----------------|
| **Windows** | `C:\Users\Public\Documents\DirektDSP\Chasm\Presets\` |
| **macOS** | `/Users/Shared/DirektDSP/Chasm/Presets/` |

The presets are organized within category folders inside the main Presets directory. Each category you create will have its own subfolder containing the individual preset files.
The default category stores the presets in this folder, not a Default subdirectory.
