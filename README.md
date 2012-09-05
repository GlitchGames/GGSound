GGSound
============

GGSound allows for easy management of sound effects and global volume in your Corona SDK powered apps.

Basic Usage
-------------------------

##### Require the code
```lua
local GGSound = require( "GGSound" )
```

##### Create your sound library
```lua
local sound = GGSound:new{ 1, 2, 3 } -- Create the library passing in some channel numbers, these should be reserved by you.
```

##### Add some sounds
```lua
sound:add( "sound1.wav", "sound1" )
sound:add( audio.loadStream( "sound2.wav" ), "sound2" ) -- A preloaded sound.
```

##### Set the volume
```lua
sound:setVolume( 0.8 )
```

##### Play a sound
```lua
sound:play( "sound2" )
```

##### Disable all playback. Useful for debugging
```lua
sound.enabled = false
```

##### Remove a sound
```lua
sound:remove( "sound2" )
```

##### Remove all sounds
```lua
sound:removeAll()
```

##### Destroy the library
```lua
sound:destroy()
sound = nil
```

Update History
-------------------------

##### 0.1
Initial release