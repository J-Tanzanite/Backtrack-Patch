# Jay's Backtrack Patch
This backtrack patch is from Little Anti-Cheat (My own project), but as a standalone plugin.

Little Anti-Cheat: https://github.com/J-Tanzanite/Little-Anti-Cheat/

## Note:
This is an early release, expect things to change!\
Currently thinking about changing the ConVar names, but we'll see.\
Maybe adding a config file too?

## Patching method:
This patch method basically simulates a player's tickcount (as if it incremented normally) when their tickcount suddenly jumps/spikes above the tolerance set by the Convar below.\
This does not happen to players who recently spawned or teleported (Via a TF2 teleporter).

Players who don't cheat but lag (packetloss) shouldn't be affected much, you have to lag quite hard for this to be an issue, which at that point, your hitreg will be awful anyway.\
If this is a concern to you, set the Tolerance to 2.

## ConVars:
`jay_backtrack_enable 1`\
Enable the backtrack patch.

`jay_backtrack_tolerance 0`\
Sets the tolerance for tickcount changes.\
0 = Tickcount must increment.
- This happens for most players 99% of the time.
- Recommended value.

1 = Allow tickcount to unexpectedly be off by 1.
- This can happen with somepacket loss, but isn't often.

2 = Allow tickcount to unexpectedly be off by 2.
- Cheats could exploit this to somewhat get around the patch, but it's so tiny, it barely helps them.
- It's not recommended to use this value.

3 = Allow tickcount to unexpectedly be off by 3.
- Do not use this value unless you understand what this does!
- A value of 3 means cheats could potentially bypass this patch to some degree, although not by much.
