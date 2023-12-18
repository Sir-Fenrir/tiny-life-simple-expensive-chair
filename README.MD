# An Expensive Chair for in Tiny Life
**Textures and settings made by McChicky in the Ellpeck Games Discord**

This mod is loaded using the (Simple Object Loader)[https://github.com/Sir-Fenrir/simple-object-loader] mod.

Instead of writing code, you can just create a JSON file (ending in '.simple.json'), which consists of key-value pairs, describing the object you want to add.

Here we have an example of the configuration you can use for a chair. With some comments we will clarify why the properties are needed. Note that comments can't be placed in the JSON files themselves, it will break them.

```
{
  "modId":  "ExpensiveChair", // The unique identifier for your mod
  "categories": ["Chair"],    // The categories, required for knowing what the object should do (in this case, be a chair)
  "name":  "ExpensiveChair", // This is the INTERNAL name of the object, not the one shows in menus. Should correspond with the name in the atlas file (if any) and the localization files.
  "tab": "LivingRoom", // In which tab the object should show up.
  "price": 500,
  "atlas": "ExpensiveChair", // The name of the atlas file in the same directory (if any)
  "size": [ 1, 1 ], // To describe the size of the object, in squares (first is x, second is y)
  "colorSchemes": [ "SimpleWood", "Modern" ], // The colorschemes to use.
  "actionSpots": [ // This describes how and from where a Tiny can interact with your item, play with it a bit.
	{
		"vectorX": 0,
		"vectorY": 0,
		"yOffset": -0.2,
		"direction": "Adjacent",
		"drawLayer": 1
	}
  ],
  "defaultRotation": "Down", // The default way of showing the object in the menu and in the world.
  "colorMap": [1, 0, 1]	 // The length of this corresponds to the number of layers your texture has, and the number corresponds to the colorschemes. 0 is the first one, 1, the second, 2 the third, etc.
}
```