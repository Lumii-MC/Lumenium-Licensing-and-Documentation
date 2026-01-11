**Creates a textured sphere on either client or common(server) side.**

How to implement:

```import com.lumii.lumenium.utils.render.SphereRenderer;```

## How to use:

**Client scheduling:**
```
SphereRenderer.scheduleClient(
                    new Vec3d(user.getX()+0, user.getY()+1, user.getZ()+0),
                    3f,
                    6f,
                    new Identifier("minecraft:textures/misc/white.png"),
                    1200,
                    1f,
                    false,
                    0,
                    0f
            );
```

*how it works:*

`new Vec3d(user.getX()+0, user.getY()+1, user.getZ()+0),` <--- where the sphere spawns.

`3f,` <--- initial radius.

`6f,` <--- target radius for scaling.

` new Identifier("minecraft:textures/misc/white.png"),` <--- texture used by the sphere

`1200,` <--- sphere duration (ticks). Can also use ```Integer.MAX_VALUE``` for infinite lifespan

`1f,` <--- alpha (opacity)

`false,` <--- whether fading is enabled or disabled

`0,` <--- after how many ticks to start fading (if fading is enabled)

`0f` <--- rotation speed

**Server/common scheduling:**
```
SphereRenderer.scheduleCommon(
                    (ServerWorld) world,
                    new Vec3d(user.getX()+0, user.getY()+1, user.getZ()+0),
                    3f,
                    6f,
                    new Identifier("minecraft:textures/misc/white.png"),
                    1200,
                    1f,
                    false,
                    0,
                    0f
            );
```
*how it works:*

Same as `SphereRenderer.scheduleClient`, only now with a casted argument to `ServerWorld`:

`(ServerWorld) world,` <--- Server world cast
