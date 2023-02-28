---
layout: post
author: James Hackett
---

# Firefox Vertical Tabs Setup

![](https://i.dbyte.xyz/firefox_Zah1kN9Ax.png)

## Requirements

[Tree Style Tabs](https://addons.mozilla.org/en-US/firefox/addon/tree-style-tab/)

## Procedure

First, in `about:config`, you'll need to change the value of `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`.

Then you'll need to open the "Profile Directory" by clicking on the menu -> help -> troubleshooting information.

Once that folder is open, create a folder called `chrome` inside if it doesn't already exist.

Inside the `chrome` folder, create or edit the `userChrome.css` file and add the following:

```css
/* Hide main tabs toolbar */
#main-window[tabsintitlebar='true']:not([extradragspace='true']) #TabsToolbar > .toolbar-items {
  opacity: 0;
  pointer-events: none;
}
#main-window:not([tabsintitlebar='true']) #TabsToolbar {
  visibility: collapse !important;
}

/* Hide splitter, when using Tree Style Tab. */
#sidebar-box[sidebarcommand='treestyletab_piro_sakura_ne_jp-sidebar-action'] + #sidebar-splitter {
  display: none !important;
}
/* Hide sidebar header, when using Tree Style Tab. */
#sidebar-box[sidebarcommand='treestyletab_piro_sakura_ne_jp-sidebar-action'] #sidebar-header {
  visibility: collapse;
}

/* Adding empty space for buttons */
#nav-bar {
  margin-right: 140px;
}

/* 15px for dragging whole window by mouse*/
#titlebar {
  appearance: none !important;
  height: 15px;
}

/* Fix for main menu calling by Alt button */
#titlebar > #toolbar-menubar {
  margin-top: 10px;
}

/* Move minimize/restore/close buttons to empty space */
#TabsToolbar > .titlebar-buttonbox-container {
  display: block;
  position: absolute;
  top: 17px;
  right: 1px;
}
```

## Custom Colours

Next edit the `userContent.css` file to add some custom colours:

```css
@-moz-document regexp("moz-extension://.+/sidebar/sidebar.html.*")
{
  :root,
  #background {
    background-color: rgb(
      40,
      42,
      48
    ); /* https://github.com/piroor/treestyletab/blob/0eede581d763f92344fe64b1c042839f3b8ca955/webextensions/resources/ui-color.css#L198 */
  }
}
```

## Changing the Shortcut

Edit the shortcut to allow Tree Style Tabs to be toggled with `Ctrl + Space` (or anything you like).

![](https://i.dbyte.xyz/firefox_8qipDP5Fl.png)
![](https://i.dbyte.xyz/firefox_t1OOU1Mkb.png)
