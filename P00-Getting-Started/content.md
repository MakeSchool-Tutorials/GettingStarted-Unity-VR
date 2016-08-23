---
title: How to use Unity
slug: unity-start-here
---

**Unity Editor**

Moving Around in 3d space

WASD - W is forward, A is strafe left, D is strafe right, S is backwards

Mouse - hold middle mouse button to pan the view, scroll middle mouse
wheel to go forward and backwards

Different Panels in the Unity Editor

![Unity Editor Panels](./media/image12.png)

Project

- Shows you the project folder for your project

- Everything is literally on disk -- if you erase something here it will
erase it from your disk

- If you import external packages they will be copied here into your
project

- You should organize various resource types in folders to make it easy
to find things in your project

- The project view (and most other views) have a filter field that lets
you easily search by name

- There are other tricks for searching in other ways too

Inspector

- Allows you to inspect an object that you click on

- Shows you the location and transform info for the object

- Also lets you edit properties of scripts at are attached to the object

- Some objects have built in properties that you can change

Console

- Shows messages from your scripts

- Shows error messages when there are problems in the scene

- Shows important system level info from unity

Scene Graph Panel

- Hierarchical Tree of the scene

- Allows you to parent/child objects to one another

- Parented objects share transform information

- When a parent object is disabled, all children are also disabled

- Scripts do not run on disabled objects

**Deep Knowledge:**

Unity creates a .meta file with the same name as every asset in your
project, this .meta file contains a unique GUID ID to identify your
asset within the project file. This is what .meta files are for.
Whenever you attach a script, it will attach to the object based on the
.meta ID. If you ever want to see if an asset is in use in your project
you can open the project file in a text editor and search for the GUID.

###Editor Modes

![Editor Modes](./media/image30.png)

- Play mode - runs the game, nothing will save while in play mode, so you
can tweak settings and delete or hide things to find bugs or test

- Pause mode - pause the execution while in play mode, useful for
debugging problems

- Step Next - allows you to step to the next frame, useful for debugging

###Scene View

- Shows you the game in edit mode, allows you to select objects and
modify them

- You can go into Scene view while the game is running to analyze the
playing field

###Game View

- This is how the game looks from the users perspective when it is
running, nothing can be selected

###Cameras

**There must always be 1 camera in the scene at all times**

The main view Camera is called the Main Camera

- You can add additional cameras and toggle between them, or do neat effects with multiple cameras like rendering to surfaces

- **FOV Field of View**: how tight or wide the cameras field of view is

- **Clipping Plane**: The clipping plane determines how far back the camera can see before it starts clipping objects

The Unity Coordinate System

- Unity coordinate system is left handed, X is left and right, Y is up and down, and Z is forward and backwards.

###GameObjects

- A Game Object is anything in the Unity World that you can manipulate in 3d space.  There are primitives and advanced Game Objects. You can also make blank empty game objects to parent other objects and help organize your scene.

Transforms and QWER to access different tools to manipulate objects

**Q is the Pan Tool**, allows you to drag the viewport around

**W is the translate tool**, allows you to move objects around in the world

**E is the scale tool**, allows you to change objects scale and size

**R is the rotation tool**, allows you to rotate objects in 3d space

###Lights

- Every game must have at least one light, or you won't be able to see anything.

- You can have as many lights as you want, but they have a cost.

- There are four kinds of lights: **directional**, **point**, **spot**, and **area**.

- **Directional lights** are global lights, they affect all objects.

- **Point light** is a sphere of light at a specific location

- **Spot light** is a spotlight that points at a specific location

- Realtime lighting is default, but it is expensive. You can also use light maps to bake lighting into the scene for performance gains at the expense of memory.  It should also be noted that baked light maps are static, and their objects cannot move.

- **Shadows** are also something that is expensive, there are different modes
for shadows and shadow maps as well.

- You can import custom meshes into unity, you can make these with external 3d asset programs or purchase them on the asset store.

- You can also animate meshes in interesting ways. You can import animations from other programs or use Unity’s keyframe editor to create your own animations

###Attaching Scripts

- You can drag and drop a script on an object to give it behavior or
properties. This is called attaching a component.

- Unity has a component architecture, this means that you can attach many
components to one object and they can all run together.

- You can make components depend on other components, but the best design
is one in which each component does a separate job.

###Scenes

Each Unity Project consists of a project file, and one or more Scene
files.

A Scene is a logical breakdown of a specific scene or level of your
game.

You can use Scenes for a variety of purposes:

Scenes can be dynamically loaded from disk to lower the memory of your game.

Scenes can separate out your game levels

Scenes can separate out large systems and can be combined at runtime.

We can talk more about Scenes later, for now it is just important to
know what they are.

GameObjects

Every scene contains a number of GameObjects.

Every object in the world is considered a Gameobject

Every GameObject has a Transform

A Transform describes the GameObjects position, scale, and rotation.

![The Transform of a GameObject](./media/image24.png)

Your world contains a tree of objects, this is called the **Scene Graph**

You can create your own little trees within this graph to organize your
scene.

If you have a parent node, the children of this parent will inherit
transform information from the parent. This allows you to scale,
translate, and rotate groups of objects together.

You can also disable/enable a parent to disable/enable entire groups of
children. This is a useful way to show/hide UI windows, show/hide level
elements, or enable/disable game systems.

![You can Disable/Enable GameObjects](./media/image23.png)

These are the basic GameObjects available in Unity:

Primitives

- **Cube**

- **Sphere**

- **Cylinder**

- **Plane**

- **Quad**

- **Terrain**

Meshes

- Imported mesh files from external 3d programs. You can use Blender, Maya, 3dStudio Max, or generic OBJ exporters. There are quite a few supported file formats.
