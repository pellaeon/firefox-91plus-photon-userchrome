# Restore classic Photon look on Firefox 91+

1. Enable `userChrome.css` by setting `toolkit.legacyUserProfileCustomizations.stylesheets` preference value to `true` in `about:config`.
1. Copy the `chrome` folder into your profile folder.
2. Change the `browser.tabs.tabMinWidth` preference value to `76`, which is the default value on Photon.

# Screenshots

Firefox 78 ESR:

![Firefox 78 ESR](https://raw.githubusercontent.com/pellaeon/firefox-91plus-photon-userchrome/master/screenshots/Firefox%2078%20ESR.png)

Firefox 91 with this userChrome.css:

![Firefox 91 with this userChrome.css](https://raw.githubusercontent.com/pellaeon/firefox-91plus-photon-userchrome/master/screenshots/Firefox%2091-after.png)

# Additional tweaks

This configuration contains a few non-Photon changes which I find convenient:

1. `@import "tab_line_loading_indicator.css";`
2. Disable the tab label mask, which makes the text label on the tab button hard to read.
3. Proton's enlarged close button on tabs are kept.

# Notes

This tweak is not perfect. I focused on undoing the most annoying change introduced in Proton:

1. The larger meaningless margin on the tab bar and navigation bar. See [screenshot](https://github.com/pellaeon/firefox-91plus-photon-userchrome/blob/master/screenshots/Firefox%2091-minwidth50.png).
2. "Tabs" don't look like tabs anymore. They should be connected to the parts below.
3. `tabMinWidth` is so small that only the first character of the tab title is visible when you have many tabs open.

There are many other parts changed by Proton, but these are less annoying in my opinion. If I have time, I will also try to revert them as well.

This tweak has only been tested on macOS 11.5.1 so far. I will improve it for KDE later.

# Sources

Most of the CSS files come from https://github.com/MrOtherGuy/firefox-csshacks , but I tweaked it further.
