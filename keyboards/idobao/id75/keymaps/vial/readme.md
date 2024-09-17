# Typematrix-like keymap with VIAL support for Idobao/ID75 v1 5x15 ortholinear keyboard

I use it with bépo configured system.
Compatible with VIA and VIAL. Underglow available.

Due to limitations of atmega32u4 chip, some features where disabled to get enougth space to enable VIAL based on this documentation: https://docs.qmk.fm/#/squeezing_avr. It maybe possible to reenable some of them depending on what you may need.

```
 * The firmware size is fine - 26640/28672 (92%, 2032 bytes free)
```

## List of disabled features

In rules.mk
 - SPACE_CADET_ENABLE = no
 - GRAVE_ESC_ENABLE = no 
 - MAGIC_ENABLE = no
 - MUSIC_ENABLE = no
 
 In config.h
 - #undef LOCKING_SUPPORT_ENABLE #Disables Cherry MX lock switch
 - #undef LOCKING_RESYNC_ENABLE  #Disables Cherry MX lock switch
 - #define NO_ACTION_ONESHOT     #Disables oneshots
 - #define NO_ACTION_TAPPING     #Disables tapping keys
 - #define NO_MUSIC_MODE         #Disables RGB matrix feature, you won't miss as RGB matrix is disabled too (v1 of the keeb has no RGB matrix anyway)
 - #define LAYER_STATE_8BIT      #Limits number of layers to 8, you may try up to 16 layers with `LAYER_STATE_16BIT`
 The following ones disable some underglow effects, this is a good way to limit firmware size, choose the ones you like (I kept `RGBLIGHT_EFFECT_RAINBOW_MOOD` and `RGBLIGHT_EFFECT_RAINBOW_SWIRL`)
 - #undef RGBLIGHT_EFFECT_BREATHING
 - #undef RGBLIGHT_EFFECT_SNAKE
 - #undef RGBLIGHT_EFFECT_KNIGHT
 - #undef RGBLIGHT_EFFECT_CHRISTMAS
 - #undef RGBLIGHT_EFFECT_STATIC_GRADIENT
 - #undef RGBLIGHT_EFFECT_RGB_TEST
 - #undef RGBLIGHT_EFFECT_ALTERNATING
 - #undef RGBLIGHT_EFFECT_TWINKLE
