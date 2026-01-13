**Creates a textured quad on either client or common(server) side.**

Credit to Homak for providing the renderer.

How to implement:

```import com.lumii.lumenium.utils.render.QuadRenderer;```

## How to use:

**Client scheduling:**
```
QuadRenderer.scheduleClient(
                new Vec3d(player.getX(), player.getY() + 0.2, player.getZ()),
                1f, 1f,                          
                new Vec3d(90, 0, 0),    
                1f,                              
                new Identifier("minecraft", "textures/misc/white.png"),
                6,
                true,
                1,
                true,
                0,
                5f,
                1f
        );
```

*how it works:*

`new Vec3d(player.getX(), player.getY() + 0.2, player.getZ()),` <--- where the quad spawns.

`1f, 1f,` <--- with & height

`new Vec3d(90, 0, 0),` <--- quad rotation, in this instance it is `90, 0, 0`. This makes the quad lay flat on the ground.

`1f,` <--- initial scale

`new Identifier("minecraft", "textures/misc/white.png"),` <--- file location of the texture used by the quad

`6,` <--- quad duration (ticks). Can also use ```Integer.MAX_VALUE``` for infinite lifespan

`false,` <--- whether fading is enabled or disabled

`1,` <--- after how many ticks to start fading (if fading is enabled)

`true,` <--- if scaling is enabled

`0,` <--- when to start scaling

`5f,` <--- scale factor

`1f` <--- alpha (opacity)

**Server/common scheduling:**
```
QuadRenderer.scheduleCommon(
                (ServerWorld) world,
                new Vec3d(player.getX(), player.getEyeY() + 0.2, player.getZ()),
                1f, 1f,                          
                new Vec3d(90, 0, 0),    
                1f,                              
                new Identifier("minecraft", "textures/misc/white.png"),
                6,
                true,
                1,
                true,
                0,
                5f,
                1f
        );
```
*how it works:*

Same as `QuadRenderer.scheduleClient`, only now with a casted argument to `ServerWorld`:

`(ServerWorld) world,` <--- Server world cast
