# Restore classic Photon look on Firefox 91+ (with some extra modification)

1. Enable `userChrome.css` by setting `toolkit.legacyUserProfileCustomizations.stylesheets` preference value to `true` in `about:config` (put it in address bar).
2. Copy the `chrome` folder into your profile folder. You can easily find it by going to `about:support` address and clicking open directory near `Profile Directory` line.
> **Optional:** Change the `browser.tabs.tabMinWidth` preference value to `76`, which is the default value on Photon.

# Screenshots

Firefox 82:

![Firefox 82](https://raw.githubusercontent.com/makzef/firefox-photon-userchrome/master/screenshots/firefox_82.png)

Firefox 98 with this userChrome.css:

![Firefox 98 with this userChrome.css](https://raw.githubusercontent.com/makzef/firefox-photon-userchrome/master/screenshots/tweaked_firefox_98.png)

Firefox 98 (dark theme) with this userChrome.css:

![Firefox 98 (dark theme) with this userChrome.css](https://raw.githubusercontent.com/makzef/firefox-photon-userchrome/master/screenshots/tweaked_firefox_98_dark.png)

# Additional tweaks

This configuration modify and even disable some additional tweaks from its parent project:

1. Disable loading indicator on top of tab (line `@import "tab_line_loading_indicator.css"`);.
2. Some changes for tab height and new tab button indents.
3. Trying to make tab close button bigger, like it was in Photon.
4. Media (audio) button on tabs were modified, keep it above favicon (in rare cases can be glitchy and replace the favicon icon).  
But it's not in the Photon style, which puts the mute button next to the left of close button. Because Proton changed the HTML structure of the mute button, it would be difficult to put the mute button back to the Photon position, so instead I moved the mute button to become "superscripted" to the favicon, similar to how Proton handle mute buttons on pinned tabs.

# Notes


This tweak is my version of firefox chrome css photon style.It's not perfect (as the original author said). I just modify it accorfing to my preferences.  
The original author focused on undoing the most annoying change introduced in Proton:

1. The larger meaningless margin on the tab bar and navigation bar.
2. "Tabs" don't look like tabs anymore. They should be connected to the parts below.
3. `tabMinWidth` is so small that only the first character of the tab title is visible when you have many tabs open. See [screenshot](https://github.com/pellaeon/firefox-91plus-photon-userchrome/blob/master/screenshots/Firefox%2091-minwidth50.png).

Maybe I will make other modifications to this project, but for now it more or less convinient for me.

This tweak has been tested on Arch Linux KDE (Manjaro and EndeavourOS), Windows 10 and also macOS 12 (however I manually make some changes like increase by 1px a line above tab). 

# Sources
Also in this project were used code from other repositories like:
*  https://github.com/pellaeon/firefox-91plus-photon-userchrome (from which I made this fork)
* https://github.com/black7375/Firefox-UI-Fix/tree/photon-style

Also useful [reddit post](https://www.reddit.com/r/firefox/comments/p3udv4/firefox_91_proton_feedback_megathread/) for Firefox Photon theming.  
Thank you to all the people for this information and code! 

# License

Mozilla Public License 2.0
