# blender project 
Creating a 3D reflection of the moon in Blender is a great project that combines aspects of modeling, texturing, and lighting. Here's a step-by-step guide to help you get started:

### 1. Set Up Your Scene
1. **Open Blender** and start a new project.
2. **Delete the default cube** by selecting it and pressing `X`, then `Enter`.

### 2. Create the Moon
1. **Add a UV Sphere**:
   - Press `Shift + A` and select `Mesh` > `UV Sphere`.
   - In the bottom-left corner, you'll see the "Add UV Sphere" panel. You can increase the segments and rings for a smoother surface.

2. **Scale the Sphere**:
   - Press `S` to scale the sphere to the desired size of the moon.

### 3. Texture the Moon
1. **Switch to the Shading Workspace**:
   - Click on the "Shading" tab at the top of Blender.

2. **Add a Material**:
   - Select the sphere, then in the "Material Properties" tab, click "New" to add a new material.
   - Name your material something like “MoonMaterial”.

3. **Add a Moon Texture**:
   - Find a high-resolution moon texture (you can search for free ones online).
   - In the Shader Editor, add an `Image Texture` node (`Shift + A` > `Texture` > `Image Texture`).
   - Open your moon texture image and connect the `Color` output to the `Base Color` input of the `Principled BSDF` shader.

### 4. Create the Reflective Surface
1. **Add a Plane**:
   - Press `Shift + A` and select `Mesh` > `Plane`.
   - Scale the plane to be larger than the moon to act as the reflective surface.

2. **Add a Material to the Plane**:
   - With the plane selected, go to the "Material Properties" tab and create a new material.
   - Name it “ReflectiveMaterial”.

3. **Set Up the Reflective Material**:
   - In the Shader Editor, use a `Principled BSDF` shader.
   - Increase the `Metallic` value to 1.0 to create a reflective surface.
   - Reduce the `Roughness` value to make the reflection clearer.

### 5. Position Your Camera and Lights
1. **Add a Camera**:
   - Press `Shift + A` and select `Camera`.
   - Move the camera to frame the moon and the reflective surface. Use `N` to bring up the transform panel for precise positioning.

2. **Add Lights**:
   - Add a `Light` (e.g., `Point Light`, `Sun`, or `Area Light`) by pressing `Shift + A` and selecting `Light`.
   - Position the light to illuminate the moon and the reflective surface properly. Adjust the light's strength and position as needed.

### 6. Render Settings
1. **Set Up Rendering**:
   - Go to the "Render Properties" tab.
   - Choose `Cycles` as the render engine for more realistic reflections, or use `Eevee` for faster previews.

2. **Adjust Render Settings**:
   - Under `Render Properties`, adjust the settings such as `Samples` for quality.
   - Enable `Screen Space Reflections` if using Eevee, and make sure to check `Refraction` and `Reflections` in the settings.

### 7. Render Your Scene
1. **Go to the "Render" menu** and select `Render Image` (F12) to generate the final render of your scene.

2. **Save the Render**:
   - After rendering is complete, you can save your image by going to `Image` > `Save As` in the render window.
