**Creates a textured beam on either client or common(server) side.**

How to implement:

```import com.lumii.lumenium.utils.render.BeamRenderer;```

## How to use:

**Client scheduling:**
```
BeamRenderer.scheduleClient(
                    new Vec3d(user.getX(), user.getY()-5, user.getZ()),
                    1f,
                    1f,
                    600f,
                    new Identifier("minecraft:textures/misc/white.png"),
                    20,
                    1f,
                    true,
                    15,
                    1f,
                    10f,
                    0f
            );
```

*how it works:*

`new Vec3d(user.getX(), user.getY()-5, user.getZ()),` <--- where the sphere spawns.

`1f,` <--- radius X

`1f,` <--- radius Z

`600f,` <--- beam height

`new Identifier("minecraft:textures/misc/white.png"),` <--- texture used by the beam

`1200,` <--- beam duration (ticks). Can also use ```Integer.MAX_VALUE``` for infinite lifespan

`1f,` <--- alpha (opacity)

`false,` <--- whether fading is enabled or disabled

`0,` <--- after how many ticks to start fading (if fading is enabled)

`1f,` <--- initial scale

`10f,` <--- target scale

`0f` <--- rotation speed

**Server/common scheduling:**
```
BeamRenderer.scheduleCommon(
                    (ServerWorld) world,
                    new Vec3d(user.getX(), user.getY()-5, user.getZ()),
                    0.5f,
                    0.5f,
                    600f,
                    new Identifier("minecraft:textures/misc/white.png"),
                    20,
                    1f,
                    true,
                    15,
                    1f,
                    10f,
                    0f
            );
```
*how it works:*

Same as `BeamRenderer.scheduleClient`, only now with a casted argument to `ServerWorld`:

`(ServerWorld) world,` <--- Server world cast
