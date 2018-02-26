# Jauke's TODO-LIST for RMEx

### scripts-externalizer

- [x] **Add** parameter: `EXTRACT_TO = "Scripts"`
- [x] **Read** Scripts.rvdata2 paths in Game.ini
- [ ] **Read** its own =begin...=end to add scripts-loader

### scripts-loader

- [x] **Add** parameter: `LOAD_FROM = "Scripts"`
- [ ] **Add** absolute/relative path recognition

### scripts-compiler

- [x] **Add** parameter: `COMPILE_FROM = "Scripts"`
- [x] **Read** Scripts.rvdata2 paths in Game.ini
- [ ] **Add** absolute/relative path recognition

### orms

- [x] **Verify/fix** compatibility between `PIXELATE_SCREEN` and some nervous scripts
    - [x] RME (camera commands)
    - [x] Luna Engine
    - [ ] Theo's Sideview battle system
    - [ ] MGC's mode 7
- [x] **Fix** name input
- [ ] **Fix** current feature status not saved in save files yet
- [ ] **Fix** characters direction in save/load menus (when `OLD_CHARSET_DIRECTION` is used)
- [ ] **Add** the feature `NO_MAP_SHADOWS` in `DESTROY_NEW_RM_FEATURES` to deactivate the VXA shadow display in maps ingame
- [ ] **Extend** `OLD_CHARSET_DIRECTION` behaviour: Will not change the directions of the Characters that the first character of their names is `'@'`.
- [ ] **Implement** `ICONS_FOR_ALL_TEXTS` feature to use the `\I[id]` control character for everything like RM2K(3) did with glyphs ($a..$Z)
- [ ] **Implement** `BITMAP_FONT_FEATURE_OPTIONS`:
    - [ ] **Define** `BITMAP_FONTS = [args_1, args_2, args_3]` option with `args_X` equal to `[name, *char_width, *char_height, *color_set, *nb_color_max, *shadow]`, for instance, `args_1` will be equal to `["Font"]` (The default font name)
    - [ ] **Define** `CURRENT_BMP_FONT`, `DEFAULT_COLOR_SET`, `DEFAULT_FONT_WIDTH`, `DEFAULT_FONT_HEIGHT`, `DEFAULT_SHADOW` options (the last three will replace `FONT_WIDTH`, `FONT_HEIGHT` and `SHADOW`)
    - [ ] **Define** `\F[id]` control character to change the BMP\_FONT in the middle of **any** text
    - [ ] **Extend** `LINE_HEIGHT` behaviour: will be defined by an integer (like now) or the array `[top_margin, bottom_margin]` instead.
    For instance, `LINE_HEIGHT` will be equal to `LINE_HEIGHT[0] + font[:height] + LINE_HEIGHT[1]`).
- [ ] **Implement** RM2k(3)-like **transitions** features and methods that reproduce and extend all transitions behaviours from RM2k(3)! :D
- [ ] **Implement** `OLD_RM_CURSOR` feature (use a second System/Window picture to make oldschool blink like RM2k(3) (graphical switch blinking)) - Will replace the actual `STOP_CURSOR_BLINKING`
- [ ] **Implement** Sfont?
- [ ] **Develop** [orms-converter](https://github.com/RMEx/orms-converter)
- [ ] **Sleep**
- [ ] **Any suggestion? ...Bug report?** Feel free to [create an issue](https://github.com/RMEx/orms-converter/issues) or [contact me on Discord!](https://discord.gg/yRUZcdQ)

### RME

- [x] **Code** release-builder
- [x] **Give** example of new organization:
```
- dev/
    - src/
        - current RME/src/ content
        ~ _list.rb (instead of build_schema.rb)

    - doc-samples/Data/
        - current RME/project/Data/ content

    - Doc.js        
    + README.rb

- release/ (automatically generated by release-builder)
    - RME for scripters/
        - Scripts/
            - RME/
                ~ current package (with version_number added in all scripts headers)
                + _list.rb
            + _list.rb
        + scripts-loader.rb
        + scripts-compiler.rb
    - README.txt
    ~ current RME.rb (with version_number added in header)

~ .gitignore
~ CHANGELOG.md (translated in english)
~ README.rb (translated in english + enhancement)
```

### orms-converter
- [ ] **Lawl**
