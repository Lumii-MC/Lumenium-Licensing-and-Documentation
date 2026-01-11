**Makes a status effect unclearable by normal means.**

How to implement:

```import com.lumii.lumenium.utils.effect.UnclearableEffect;```

How to use:

```
public class TestEffect extends UnclearableEffect {
    public TestEffect(StatusEffectCategory category, int color) {
        super(category, color);
    }
}
```

*How it works:*

This implementation can be used for custom status effects to make them unclearable. 

Unclearable status effects can **only be cleared by dying.**
