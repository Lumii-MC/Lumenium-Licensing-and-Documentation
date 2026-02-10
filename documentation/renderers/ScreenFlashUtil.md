**Creates a flash of color on the screen.**

How to implement:

```import com.lumii.lumenium.utils.render.screen.ScreenFlashUtil;```

## How to use:

**Simple flash:**
```
ScreenFlashUtil.flash(
                255, 255, 255,
                1,
                10
        );
```

*how it works:*

`255, 255, 255` <--- Color of the flash, (float values)

`1,` <--- Alpha (Opacity, float)

`10` <--- Duration in ticks (How long the flash lasts.)

**Held flash:**
```
ScreenFlashUtil.heldFlash(
                255, 255, 255,
                1,
                10,
                100
        );
```

*How it works:*

`255, 255, 255` <--- Color of the flash, (float values)

`1,` <--- Alpha (Opacity, float)

`10,` <--- Hold duration in ticks (How long the flash is held before fading, float)

`100` <--- Fade duration in ticks (How long the flash takes to fade out completely, float)
