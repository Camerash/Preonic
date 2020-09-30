# Camerash Preonic (Rev3) Layout
This is my personal take on a Preonic keyboard layout.

## Philosophy
Coming from a traditional staggered keyboard, I focus on 3 core ideas in designing this layout:
- Shallow learning curve for traditional staggered keyboard users
- Keys on Lower / Raise layers should be memorable and feel natural to use 
- Underglow LEDs as layer indicator

## Layout
![](https://github.com/Camerash/Preonic/blob/master/layout.png?raw=true)


## Modifications
This layout is based on the [default Preonic Rev3 layout](https://github.com/qmk/qmk_firmware/tree/master/keyboards/preonic/keymaps/default), and modifications includes (but not limited to) the following:
- Keys:
  - Removed `Dvorak` and `Colemak` layout options
  - Combine `Esc`(*Base*), `~`(*Lower*) and `` ` ``(*Raise*) as a single key at top-left corner
  - Number keys act as symbols in *Lower*, and function keys in *Raise*.
  - Align *Lower* `()`, `{}`, `[]` keys in a logical and easy to memorize order
  - Left/Right arrow keys act as Prev/Next media control  in both *Lower* and *Raise*
  - Enter key act as Play/Pause media control in both *Lower* and *Raise* 
  - Up/Down arrow keys control Volume in *Lower*, and control Brightness in *Raise*
  - Most keys are identical in *Lower* and *Raise* except the symbol/function keys row
  - In *Adjust*, keys for keyboard settings and maintainance stays on the left, while a keypad layout is available on the right
- Visual:
  - Underglow LEDs' color will react to layer changes:
    - Base - Purple
    - Lower - Blue
    - Raise - Red
    - Adjust - Cyan
- Audio:
  - The option of disabling audio in my default Preonic is somehow non-persistant, and the startup sound will play every single time I replug the keyboard. A although I didn't change anything for audio in my layout, this issue is somehow solved by flashing a new firmware.

## Customization
You can customize the keymap to your heart's content, to name a few:
- Color for underglow LEDs for each layers by modifying `RGBLIGHT_LAYER_SEGMENTS`. [Docs here](https://docs.qmk.fm/#/feature_rgblight?id=lighting-layers)
- Sounds for different layers (which I disabled). [Docs here](https://docs.qmk.fm/#/ref_functions?id=setting-the-persistent-default-layer)
- Keymaps for different layer (Duh)

## Caveats
There are a number of limitations that restricted this keymap from become a better layout, namely:
- I would love to enable [Tap-Toggle](https://docs.qmk.fm/#/feature_layers?id=layers) for the Lower/Raise layer keys to for example make using the keypad layout on *Adjust* more comfortable. However, due to [the way QMK handles Tri Layers](https://docs.qmk.fm/#/ref_functions?id=olkb-tri-layers) this is currently impossible (at least to my knowledge). Closest thing I came across in my research is [enabling LT in a Tri Layer setup](https://www.reddit.com/r/olkb/comments/4x3dei/hack_too_ugly_to_live/)
- There are way too many blank keys going to waste on both *Lower* and *Raise*. While this is fine for now, I will probably start adding macro/shortcut keys as I perform more of my daily workflow with this keyboard.
- Same problem as above except this time its too many similar keys on both *Lower* and *Raise*. However this is probably for the best for a dummy like myself.

## Compiling/Flashing
1. Follow the [official QMK setup](https://docs.qmk.fm/#/newbs_getting_started)
2. [Create a new keymap for Preonic Rev3](https://docs.qmk.fm/#/newbs_building_firmware?id=create-a-new-keymap)
3. Copy everything in `layout` from this repo to the folder of your new keymap, replace when necessary.
4. Customization! :art:
5. [Build](https://docs.qmk.fm/#/newbs_building_firmware?id=build-your-firmware) and [Flash](https://docs.qmk.fm/#/newbs_building_firmware?id=flash-your-firmware) as you would with any other QMK firmware.

## Bonus
- [Where I got my Preonic kit](https://drop.com/buy/preonic-mechanical-keyboard)
