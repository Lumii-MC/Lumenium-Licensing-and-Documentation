**Makes an Item two-handed**

How to implement: 

```import com.lumii.lumenium.utils.item.TwoHandedItem;```

How to use:

```
public class TestItem extends Item implements TwoHandedItem {
  public TestItem(Settings settings){
    super(settings);
  }
}
```

*How it works:*

Simply by implementing the class, an Item is now two-handed by using `ArmPose.CROSSBOW_CHARGE`.

