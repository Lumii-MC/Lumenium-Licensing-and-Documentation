**Saves a LivingEntity from death when returned true**

How to implement:

```import com.lumii.lumenium.utils.item.KillSaveItem```

How to use:

```
public class TestItem extends Item implements KillSaveItem {
    public TestItem(Settings settings) {
        super(settings);
    }
```
```
@Override
    public boolean killEntity(World world, ItemStack stack, LivingEntity attacker, LivingEntity victim) {
        return true;
    }
```

*How it works:*

Returning `true` saves the entity from death by acting as if it had used a totem. Returning `false` does not do this, and treats death normally.

**Currently is only known to properly work on players.**
