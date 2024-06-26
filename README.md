# uslikenorsk

Uslikenorsk is designed to be an enhanced intuitive Norwegian keyboard layout that mixes the functionality of Norwegian keyboard with a more international standard
keyboard layout to help us to Code and use the terminal.

### Why I decided to use uslikenorsk?

Well, First of all I am a foreigner in Norway. And in all my jobs but the last one I had always used UNIX and Windows laptops with Norwegian layout.
So when I was told that I was going to be given a Macbook I thought to myself "Well, same same... How difficult can it be to get use?", but it did not take long to realize how naive I was!.

### Disclaimer

I have only tested this in macOS Sonoma.

## Layouts

Quick clarification: **alt** equals **option** key.

### Basic layers of the keylayout

The biggest difference is that in the basic keyboard layout we are not able to press the character **å**. But it is easily pressed using the **alt** key before pressing it (or **shift+alt+å** for **Å**)

![Image of basic layout](https://raw.githubusercontent.com/xepyon/uslikenorsk/master/images/uslikenorskBasicLayout.png)

### Shift press layout

![Image of basic layout](https://raw.githubusercontent.com/xepyon/uslikenorsk/master/images/uslikenorskShiftLayout.png)

### Alt press layout

![Image of basic layout](https://raw.githubusercontent.com/xepyon/uslikenorsk/master/images/uslikenorskAltLayout.png)

### Shift+alt press layout

![Image of basic layout](https://raw.githubusercontent.com/xepyon/uslikenorsk/master/images/uslikenorskShiftAltLayout.png)

### macOS installation

1. Move `uslikenorsk.keylayout` into `~/Library/Keyboard Layouts/`
2. Log out and log back in
3. Select the new keyboard layout from System Settings (Example for macOS Sonoma System Settings -> Keyboard -> Text Input Edit -> + -> Others -> uslikenorsk)

That is all! Have fun!

## Exchanging Left FN key with Left CTRL key

After using the keyboard layout for a while I realized that I could not get used to the **FN** key being in the left corner of the keyboard and I was constantly pressing it instead of the **CTRL** key.

If you are like me and you are used to having the **CTRL** key in the left corner of the keyboard, you can use the following command to remap the **FN** key with the **CTRL** key.

You can do a quick test until rebooting the computer by running the following command

```bash
cp ~/.local.hidutilKeyMapping.plist ~/Library/LaunchAgents/local.hidutilKeyMapping.plist
launchctl load ~/Library/LaunchAgents/local.hidutilKeyMapping.plist
```

If you are convinced you can make the changes permanent running

```bash
launchctl start local.hidutilKeyMapping.plist
```
