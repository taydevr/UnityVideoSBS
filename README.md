# Simple Video Side-by-Side (SBS) Shader

## Description

This simple shader is designed for rendering side-by-side (SBS) video in Unity. It allows you to display stereo content by adjusting UV coordinates based on the eye index. The shader takes into account the eye separation value to create a visually appealing SBS effect.

## Features

- Side-by-side (SBS) video rendering
- Compatible with Unity's Universal Render Pipeline (URP)

## Installation

1. Clone or download this repository.
2. Open your Unity project.
3. Import the shader by copying the `VideoSBSShader.shader` file into your project's `Assets` folder.

## Usage

1. **Create a Plane or Quad**:
   - In your Unity scene, create a plane or quad (3D Object > Quad or Plane).
   - Adjust the size and position of the plane according to your requirements.

2. **Create a New Material**:
   - In the Unity Inspector, right-click in the Assets panel and choose "Create" > "Material."
   - Name the material (e.g., "VideoSBSMaterial").
   - Double-click the material to open its properties.

3. **Assign the `VideoSBSShader` to the Material**:
   - In the material properties, locate the Shader dropdown.
   - Select "Custom/VideoSBS" from the list (assuming you've already imported the shader).

4. **Assign the Material to the Plane or Quad**:
   - Select the plane or quad in the Hierarchy.
   - In the Inspector, find the Renderer component.
   - Drag and drop your newly created material onto the Material field.

5. **Add a "Video Player" Component**:
   - Add a "Video Player" component to a GameObject.

6. **Assign Your Video Clip**:
   - In the Video Player component, locate the "Video Clip" property.
   - Drag and drop your video file (SBS) (e.g., an MP4 or MOV) into this field.

7. **Configure Render Mode**:
   - Still in the Video Player component, change the "Render Mode" property to "Material Override."

8. **Assign the Plane or Quad Mesh Renderer**:
   - In the Video Player component, find the "Renderer" property.
   - Drag and drop the plane or quad (with the assigned material) into this field.
   - Select `_MainTex` property in "Material Property".

## Notes

- Ensure that your video texture is properly aligned for side-by-side rendering.

## License

This shader is provided under the MIT License. Feel free to use and modify it for your projects.
