# VampireTCP

## To Do:

**SERVER**
- Customizing ports
- Setting to enable extra port for UDP (this way, packets that get sent frequently, like every frame, such that it doesn't matter if a couple get dropped, can use this port and leave the regular TCP port to handle more important, occasional packets)
- Room creation (obviously)
- Setting a room as public/private
- Get a list of all public rooms
- Custom Room class (a class that can hold methods and variables)
- Variable events (Be able to specify whether a variable, when changed, should then be rebroadcasted to all clients)
- Get/Set Custom Room variables OR methods (as set in the Custom Room class. For methods, only respond to the client if the method returns something.)
- The ability to override what happens when someone joins or leaves a room
- Multi-threading (Gotta use ***ALL EM CORES!!!***)
- A version of the server that is a headless export of the Unity game, so that users can run simulations and stuff
- A bunch of optimizations and reliability shenanigans (like storing the past 100 packets that were broadcasted to everyone, and keeping track of how many total have been sent, and keep track of how many have been received on the client, and if the client is ever less than the server, the server will take 100-numSent+numRecieved and use that as an index, sending that client all the messages stored from that point on till they're back up to date)

**CLIENT**
- Setting server + port (if UDP enabled, that port too)
- Connecting to a server
- Creating a room (public or private)
- Joining a room
- Getting a list of all public rooms
- Disconnecting from a room
- Disconnecting from a server
- Creating Globally Unique Objects (Objects that basically exist in exactness on every client, same properties and component data and such, basically there's only one of them.

**PREFABS/PREMADE SCRIPTS**
- Network Manager Prefab
- GUO Script
- Headless Server Prefab
- Server PY/Go Script
