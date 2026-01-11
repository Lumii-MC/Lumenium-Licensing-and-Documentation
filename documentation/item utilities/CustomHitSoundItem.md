**Makes an item play a custom sound on hit.**

How to implement:

```import com.lumii.lumenium.utils.item.CustomHitSoundItem;```

How to use:

```
public class TestItem extends Item implements CustomHitSoundItem {
    public TestItem(Settings settings) {
        super(settings);
    }
```
```
@Override
    public SoundEvent getHitSound(World world, ItemStack stack, LivingEntity attacker, LivingEntity target) {
        return SoundEvents.BLOCK_BELL_USE;
    }

    @Override
    public float getHitPitch(ItemStack stack) {
        return 1f;
    }

    @Override
    public float getHitVolume(ItemStack stack) {
        return 1f;
    }
```

*How it works:*

The first Override defines the SoundEvent to use on hit. This can also be a custom sound effect.

The second override determines the pitch via the returned value **above** `0f`.

The third Override determines the volume via the returned value **above** `0f`.
