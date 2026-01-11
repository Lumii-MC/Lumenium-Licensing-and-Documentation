**Runs code when killing a LivingEntity**

How to implement:

```import com.lumii.lumenium.utils.item.OnKillEffectItem;```

How to use:

```
public class TestItem extends Item implements OnKillEffectItem {
  public TestItem(Settings settings){
    super(settings);
  }
}
```
```
@Override
    public void onKill(World world, ItemStack stack, LivingEntity attacker, LivingEntity victim) {
    }
```

*How it works:*

In the Override, any code implemented will run upon killing the victim. For example:

```
@Override
    public void onKill(World world, ItemStack stack, LivingEntity attacker, LivingEntity victim) {
    victim.setHealth(1f);
    }
```

This will set the victim's health to 1 every time it is killed with this item.
