# **Houdini mask generator**

## Introduction
The Mask Generator tool is used to generate masks on the point level for geometry.
The tool generates Ambient Occlusion, Direction, Height, Noise and Slope masks.

These masks can be combined via multiparm instances and have various Combine Method options, such as Add, Sub, Mult, Div and so on.

**Example of a few the tool looks when used on Tommy.**

![](Images/mask_demo.jpg)
![](Images/params.jpg)

## **How to use the tool** 

### **Getting the tool**

To get the tool:
1. Go to the main tool page and download https://github.com/ognyan97/Houdini-Masking-Generator-/blob/main/sop_ot.dev.mask_generator.1.0.hdalc . 
![](images/how_to.jpg)
2. Import it to your local Houdini HDA / OTL library. (this of course varies from user to user).
3. Open Houdini
4. Import the .HDALC file through FILE -> Import -> Houdini Digital Asset...

![](Images/import.jpg) 

![](Images/install.jpg)

### **Using the tool**

Once installed, the tool will be available as a SOP level node.
Go into your graph and look for it under the Digital Assets list in your **tab** menu.
Once dropped, wire it into any polygonal mesh you have et voilà! 

### **Parameters**

The Mask Generator has two types of parameters, top and sub-parameters.

#### **Top Parameters** 

The top parameters are:

1. Visualize Mask  - Used to visualize the mask (duh).
2. Base Mask Value - Used to set the 0-100 level of the mask. 
   
     2.1. This is impacted by all mask attributes. Most are in the 0-1 range, but this has been set 0-100, because I've found most people find it easier to understand when it's represented in a percentage range, but in reality, this value gets refitted in a 0-1 range under the hood.
3. Mask Colour     - Used to set the colour of the mask when visualizing it on the mesh.

#### **Sub Parameters**

The contextual sub-parameters only appear under certain conditions. More specifically, they're all tied with the type of mask you're trying to generate.

The non-contextual ones parameters are:

1. Mask Type       - Used to select what kind of mask to generate on the surface.
2. Combine Method  - Used to select the combine method for the masks.

**The Mask type are:**

1. Ambient Occlusion
2. Height
3. Slope
4. Direction
5. Noise

All of them have their own respective paremeters. More on that below.

**The Combine Methods are:**

1. Add
2. Subtract
3. Multiply
4. Divide
5. Blend
6. Screen
7. Overlay
