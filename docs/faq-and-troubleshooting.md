# **FAQ and Troubleshooting**

## Why are my layers rendering in black without color?

The selected layers rendering only in black is a common issue caused by not having any lighting layers selected. To fix this problem, there are a few options:
1. Ensure a layer with a global light object is selected.
2. Use other non-global light sources and ensure that their layer is selected.
3. Change the material of the Sprite Renderers of the game objects on the selected layer to Sprite-Unlit-Default.

## Why are the selected layers expanding and color bleeding?
This is a recursive rendering issue caused by having the renderer index set to the same value as the renderer that has the render feature attached.

It will continuously render the selected layers through the same renderer, creating a bleeding effect.

To fix this issue, simply create a second renderer and assign the renderer index to the new renderer.
