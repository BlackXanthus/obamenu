# obamenu
Obamenu 1.1.8

Obamenu is the grandfather of creating menues on Openbox. 

However, overtime it has languished at version 1.1.7, with no active development. In truth, there has been
very little need for development of this little script - yet time has not been kind. 

Standards have changed, and the once icon-filled menu has lanugished. This version will now include the default icons
if the other icons are not found.

As .desktop files are also used to control interaction with MIME types, obamenu ends up installing several copies of the same
icon. This version attempts to remove such duplicates (with varying success)

It also includes better support for programs that require complex starting paramaters, like GIMP 2.10, which is a flatpack
piece of software so wouldn't start using the old obamenu. This has been fixed by a re-working of the process
used to create menu items. 

This version is still under development, but the Master branch is stable and eminantly usable.

**Installation:**

1. Download the file 'obamenu', and unpack it somewhere. 
2. Edit your menu.xml file (normally found in ./config/openbox/)
3. Insert the following lines: 
```
 <menu execute="/location/to/obamenu/obamenu" id="My Menu" label="My Menu" />
 ```
 Make sure that you use the full path to the location of the script. 
 
 4. Reconifigure openbox
 5. You should now see a new menu item labelled "My Menu". If you hover over that, it should open as you would expect the menu too.
 
 The MASTER branch contains the most up-to-date stable code. Use this for preference. 
 The RELEASED code contains the code that achieved the basic aim of updating obamenu to have sensible settings, icons, and file search locations. 
 
 NOTE: This version of Obamenu does not ignore applications (as the previous version did). It also, however, doesn't search down GNOME/KDE locations to find software. As such, these items may not show up in the default install.
 
 NOTE: Openbox does cache dynamic menues(it does this behind the scenes), as such if you use the default obamenu, AND THEN use this menu, you may find that icons will be back missing. Wait a few moments, then try again. 
