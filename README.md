# 3D Mesh Render
This was originally a code challenge for InkBit back in 2020. It is for loading and visualizing 3D models for 3D printer applications.
It uses ThreeJS and WebGL.

## To run 
>npm install
>node uiserver.js

In a webbrowser go to localhost:9000

Tested on Chrome and Windows 10.

source code:
https://github.com/mrdoob/three.js/

Interactive demos.
https://threejs.org/examples/#misc_controls_transform

For more information, go to "./doc" folder.

## Features Added
### Basic Functions:
- Added the basic functionality of uploading an STL
  - Converted to mesh and added to scene
- It puts the mesh on the lower left corner and snaps it to the floor
-   Uses its bounding box to translate the mesh so that it is flush with plane

### Select Mesh:
- You can select different meshes
- The mesh your cursor is over will be highlighted
  - Used a raycaster for this
- The controls will switch to the selected mesh (once you click it)
- You can press “ESC” to deselect

### Delete Mesh:
- If you press “delete”, the currently selected mesh will be deleted

### Duplicate Mesh:
- You can duplicate the selected mesh by pressing “D”

### Save Mesh List:
- Click the “SAVE MESH LIST” button and it will save all the meshs’ filenames, positions, and rotations

### Future Improvements:
- Rewrite it so that the JavaScript doesn’t use global variables
- Make the data immutable so that it would be easier to test. And/or convert it into a React project as suggested.
- Write tests! (like with Jest, for instance) I know the code is quite breakable right now since I didn’t write tests for it…


