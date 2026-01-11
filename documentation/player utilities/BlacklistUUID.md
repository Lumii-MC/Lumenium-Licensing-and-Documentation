**Blacklists a player's UUID via a client crash when loading into a world.**

How to implement:

```import com.lumii.lumenium.utils.player.BlacklistUUID;```

How to use:

```BlacklistUUID.uuid("uuid-here");``` <--- This method blacklists a single UUID.

```BlackListUUID.uuidList("uuid1", "uuid2", "uuid3");``` <--- This method blacklists a list of UUIDs up to 3.

*How it works:*

If the local player's UUID matches an inputted UUID, the client will crash and give crash report:

  `Caused by: java.lang.RuntimeException: Player is blacklisted via Lumenium.`
