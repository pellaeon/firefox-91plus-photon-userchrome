# Restore classic Photon look on Firefox 91+

1. Enable `userChrome.css` by setting `toolkit.legacyUserProfileCustomizations.stylesheets` preference value to `true` in `about:config`.
2. Also in `about:config`, set `browser.nova.enabled` to `false`. ([Ref](https://blog.mozilla.org/addons/2026/09/29/nova-is-here-what-changes-for-your-firefox-theme/))
3. Copy the `chrome` folder into your profile folder. (Profiles on Linux are under `~/.mozilla/firefox/`.)
 
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

1. The larger meaningless margin on the tab bar and navigation bar.
2. "Tabs" don't look like tabs anymore. They should be connected to the parts below.

This project is tested on Firefox 159 under KDE.

# Sources

Most of the CSS files come from https://github.com/MrOtherGuy/firefox-csshacks , but I tweaked it further.

# License

Mozilla Public License 2.0
