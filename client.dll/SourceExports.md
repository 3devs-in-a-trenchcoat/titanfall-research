# What
Source Engine uses a funny format for externing classes.
It creates a giant linked list of them under a function called `CreateInterface`.

For more information see here:
https://github.com/ValveSoftware/source-sdk-2013/blob/master/mp/src/tier1/interface.cpp#L56
https://github.com/ValveSoftware/source-sdk-2013/blob/master/mp/src/public/tier1/interface.h#L87

# Interfaces dumped with static analysis
```
ClientRenderTargets001
GameClientExports001
VClientDllSharedAppSystems001
VClient018
VClientEntityList003
ClientLeafSystem002
IEffects001
VParticleSystemQuery004
VClientPrediction001
GameMovement001
GameConsole004
GameUI011
RunGameEngine005
VCLIENTTOOLS001
```
These are only the interfaces I could find in the client.dll image.
