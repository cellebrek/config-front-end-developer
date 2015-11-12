# ATOM

This file for Atom IDE configuration


## Own configuration for perform on Atom

* Main Atom config

Need to edit config.cson in .atom
add this

```shell
	"*":
  "exception-reporting":
    userId: "b6c6e785-0b6e-3cf6-78d9-54030c89effb"
  welcome:
    showOnStartup: false
  editor:
    invisibles: {}
    tabLength: 4
    showIndentGuide: true
  core:
    packagesWithKeymapsDisabled: [
      "bracket-matcher"
    ]
    disabledPackages: [
      "merge-conflicts"
    ]
  emmet: {}
  "merge-conflicts": {}
  "atom-terminal": {}
  "bracket-matcher": {}
  "atom-format": {}
```

* Emmet manuel config about stylus autocompletion with Separator ':' / ';'

Need to edit & modify css.js in .atom/packages/emmet/node_modules/emmet/lib/resolver/
On line 113 to 118 copy this

```shell
prefs.define('stylus.valueSeparator', ': ',
'Defines a symbol that should be placed between CSS property and '
+ 'value when expanding CSS abbreviations in Stylus dialect.');
prefs.define('stylus.propertyEnd', ';',
'Defines a symbol that should be placed at the end of CSS property  '
+ 'when expanding CSS abbreviations in Stylus dialect.');
```

* Keybinding config

Need to edit keymap.cson in .atom
add this

```shell
'atom-text-editor[data-grammar="text html php stylus handlebars twig"]:not([mini])':
    'tab': 'emmet:expand-abbreviation-with-tab'
```
