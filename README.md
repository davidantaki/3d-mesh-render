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
![image](https://user-images.githubusercontent.com/36055788/219108877-66b9f075-4ff6-4cf4-8038-6a34fd8a5b04.png)

### Select Mesh:
- You can select different meshes
- The mesh your cursor is over will be highlighted
  - Used a raycaster for this
- The controls will switch to the selected mesh (once you click it)
- You can press “ESC” to deselect
![image](https://user-images.githubusercontent.com/36055788/219108964-48edeb69-e52e-456e-bd28-64bc4c2cd21b.png)
![image](https://user-images.githubusercontent.com/36055788/219109037-2776c183-74be-44e3-90ec-889615189572.png)


### Delete Mesh:
- If you press “delete”, the currently selected mesh will be deleted

### Duplicate Mesh:
- You can duplicate the selected mesh by pressing “D”
![image](https://user-images.githubusercontent.com/36055788/219109403-0f8e1189-ba54-4930-98cf-3954912247fa.png)

### Save Mesh List:
- Click the “SAVE MESH LIST” button and it will save all the meshs’ filenames, positions, and rotations
![image](https://user-images.githubusercontent.com/36055788/219109571-9e232923-7120-4a18-9d7a-2912bcc5f875.png)


### Future Improvements:
- Rewrite it so that the JavaScript doesn’t use global variables
- Make the data immutable so that it would be easier to test. And/or convert it into a React project as suggested.
- Write tests! (like with Jest, for instance) I know the code is quite breakable right now since I didn’t write tests for it…


