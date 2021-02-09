# Unleash-Your-Potential-Theme
![screenshot](https://github.com/CuteBlueRadio/Unleash-Your-Potential-Theme/blob/main/Screenshot%20from%202021-02-09%2016-37-28.png?raw=true)

#### Dependencies
* devilspie
* conky
* cli-visualizer
* Terminator

### Configuration

#### conky

Place the conky.conf file in your conky .config folder. If you already have a configuration file for conky, simply replace it or include both. If you have multiple configure files you will have to run conky with ```conky -c .config/FILE.conf```

The conky configuration included was based off of https://github.com/brndnmtthws/conky/wiki/configs/ze/conkyrc.

#### cli-visualizer (vis)

Just like with conky, take the vis_colors file and place it in the .config/vis/colors/ folder. You will have to either change its name to 'colors' or add it to the color.scheme list in .config/vis/config. Values are seperated by ',' and nothing else. For example:


colors.scheme=vis_colors

when executing 'vis' in your terminal the blue-yellow theme should show.

#### Terminator and Devilspie

Place the devilspieconf.ds in your .devilspie folder. Devilspie will now find any application named "terminator", stick it, make it "always below", undecorate it, and make it the "dock" window type.

Run devilspie in debug mode to make sure there are no errors with 

```devilspie --debug```

Open up Terminator and go to the preferences menu.

* check "Show on all workspaces"
* check "Hide from taskbar"
* in "Profiles" go to the command tab and add the custom command "vis". This will launch the visualizer every time the terminal opens.
* under "Background" set the background to transparent
* under scrolling disable scrolling

Move and resize the window into the positition you want it to be in. When you're ready, go to "Layouts" in the terminator prefrences and select "Add" and "Save"

Now we will edit the terminator config file so that your layout begins with every Terminator startup. Edit the config file in .config/terminator/ and delete the [[default]] layout under [layouts]. Rename your [[New Layout]] to [[default]]. Save and Close.

Now close Terminator and try opening it up again. It should open with cli-visualizer open and running with your custom profile.

Run ```devilspie``` in another terminal and Terminator should be suppressed back into the desktop.

Finally, add the commands ```terminator```, ```devilspie``` and ```conky``` to your startup applications using the Startup Applications app. Every time you boot up everything should smoothly start in your desktop!
