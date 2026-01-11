**Changes the color of an ItemStack's name.**

How to implement:

```import com.lumii.lumenium.utils.generic.CustomItemNameColor;```

How to use: 
```
public class TestItem extends Item implements CustomItemNameColor {
  public TestItem(Settings settings){
    super(settings);
  }
}
```
```
@Override
    public int getHexColor(ItemStack itemStack) {
        return 0xFF004F;
    }

    @Override
    public Text getName(ItemStack stack) {
        return getColoredName(stack);
    }
```

*How it works:*

```
@Override
    public int getHexColor(ItemStack itemStack) {
        return 0xFF004F;
    }
```

This Override sets the item's name color to the returned value (FF004F, Folly)

```
@Override
    public Text getName(ItemStack stack) {
        return getColoredName(stack);
    }
```

This Override gets the returned value from the previous Override and changes the default color of the item's translation key to the set color.

These two Overrides work together to set a custom item name color. Remember to keep the hex code ***AFTER*** the `0x` in the first Override, or else it won't work!
