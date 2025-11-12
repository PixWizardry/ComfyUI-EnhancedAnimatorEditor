# Enhanced Animator Path Editor for ComfyUI
![Tested ENV](https://img.shields.io/badge/Tested%20ENV:-lightgrey)
![Python 3.12.x](https://img.shields.io/badge/Python-3.12.x-76B900) 
![Pytorch Ver 2.10](https://img.shields.io/badge/Pytorch-2.10.0-76B900)
![Cuda Ver 13.0](https://img.shields.io/badge/Cuda-13.0-76B900)
![Platform Windows](https://img.shields.io/badge/Platform-Windows-76B900)


This project is a modification of the original `FL-Path-Animator` by Machine Delusions from the Fill-Nodes pack. The core functionality has been significantly extended with professional-grade features.

## Key Enhancements Over the Original Version

This version is a major upgrade from the original node. The entire editor experience has been overhauled for a more powerful and intuitive workflow.

#### **1\. Professional Canvas Navigation & Workflow**

* **Full Zoom & Pan:** The canvas is no longer static. Seamlessly zoom in on details (`Ctrl + Mouse Wheel`) and pan across your workspace (`Middle-Mouse Drag`).  
* **Grid & Snapping System:** A fully customizable grid system has been added. You can toggle visibility, enable snap-to-grid for precision, and control the grid's size, color, and opacity.  
* **Compositional Guides:** Drastically improve your animations with built-in compositional overlays like the Rule of Thirds, Golden Ratio, Diagonals, and more. You can even load your own **SVG file** as a custom guide.  
* **Non-Destructive Resizing:** The new resizing tool lets you change the canvas to standard aspect ratios (16:9, 1:1, etc.) without losing the quality of your original background image, allowing you to re-frame your work at any time.

#### **2\. Advanced Drawing & Manipulation Tools**

* **New `Orbit Tool`:** Effortlessly create perfect circular or elliptical orbit paths.  
* **New `Zoom Box Tool`:** A unique and powerful tool for creating complex zoom animations. Draw a box, and use the mouse wheel to generate four perfectly synchronized corner paths.  
* **Path Manipulation:** Go beyond drawing and deleting. You can now **clone** any selected path and **flip it horizontally or vertically**.

#### **3\. Modernized User Interface**

* **Redesigned UI:** The editor interface has been completely upgraded with  more buttons, and dedicated control panels for different functions.  
* **Improved Controls:** Sliders now include precise number inputs, and the toolbar has been expanded to accommodate the new creative tools.

#### **4\. Dynamic Animation Controls**

* **Global Timeline:** In addition to per-path timelines, you can now set a global `start_time` and `end_time` percentage to constrain all animations to a specific window.  
* **Speed Boost:** A new `speed_boost` parameter allows you to change the speed of an animation without redrawing the path. This works by dynamically scaling the path's length, making it a powerful tool for timing and iteration.

---

### Animation & Output Features

* **Speed & Distance Control:** Modify path lengths dynamically with `override_path_length` and `speed_boost` to simulate changes in speed without redrawing.  

### Enhanced Animator Path Editor Features

* **Advanced View Controls:**  
  * **Zoom & Pan:** Seamlessly navigate the canvas using `Ctrl + Mouse Wheel` to zoom and `Middle-Mouse Drag` to pan.  
  * **Grid System:** Enable a customizable grid with snapping for precise path placement. Control grid size, color, and opacity.  
* **Powerful Drawing Tools:**  
  * **Pencil & Static Point:** Draw freeform motion paths or place single static points.  
  * **Orbit Tool:** Easily create perfect circular or elliptical orbit paths.  
  * **Zoom Box Tool:** A unique tool to generate four coordinated paths from the corners of a resizable box, perfect for creating zoom-in/out effects.  
* **Compositional Aids:**  
  * **Built-in Guides:** Overlay compositional guides like Rule of Thirds, Golden Ratio, Center Cross, Diagonals, and more.  
  * **Custom SVG Guides:** Load your own SVG file to use as a custom guide or tracing template.  
* **Efficient Workflow:**  
  * **Non-Destructive Resizing:** Resize the canvas and background image to standard aspect ratios (16:9, 1:1, etc.) while preserving the original high-resolution image for future adjustments.  
  * **Path Manipulation:** Clone, flip horizontal, and flip vertical for any selected path.  

## Usage

1. **Add the Node:** In ComfyUI, add the `Enhanced Animator Path Editor` node to your workflow.  
2. **Open the Editor:** Click the **`Edit Paths`** button on the node to open the Advanced Path Animator editor.  
3. **Set Background (Optional):**  
   * Click the "Load Background Image" button to load a reference image.  
   * Or, simply paste an image from your clipboard using `Ctrl+V`.  
4. **Draw Paths:** Use the tools in the left-hand toolbar to draw your motion paths or place static points. Use the zoom and pan controls to navigate.  
5. **Adjust Paths:**  
   * Select a path by clicking on it in the canvas or in the right-hand sidebar.  
   * In the sidebar, adjust the path's name, timeline (start/end time), interpolation (easing), and visibility mode.  
6. **Save & Close:** Click **`Save Paths`** to save your work and close the editor. The `paths_data` widget on the node will be updated.  
7. **Configure Node Settings:** Adjust the main node parameters like `shape`, `shape_size`, `frame_count`, `speed_boost`, etc.  
8. **Connect Outputs:**  
   * `image`: The rendered animation as an image batch.  
   * `mask`: A corresponding mask batch.  
   * `coordinates`: The JSON string of 121-point resampled paths for use with nodes like WAN-ATI.

## Path Editor Tools

| Tool | Icon | Description |
| :---- | :---- | :---- |
| **Pencil** | ✏️ | Draw freeform motion paths. Hold `SHIFT` for straight lines or any angle. |
| **Orbit** | 💫 | Click to set a center point, then drag to define the shape of an elliptical path. |
| **Zoom Box** | 🔳 | Draw a rectangle. Use the mouse wheel to scale it, creating four corner paths. **Right-click to finalize.** |
| **Static Point** | 📍 | Click to add a single, non-moving anchor point. |
| **Select** | 🖱️ | Select, move, and edit paths and their individual points. |
| **Eraser** | 🗑️ | Click on a path to delete it. |
| **Clone** | 📋 | Duplicates the currently selected path. |
| **Flip H/V** | ↔️ / ↕️ | Flips the selected path horizontally or vertically across its center. |
| **Reset View** | 🔄 | Resets canvas zoom and pan to the default view. |
| **Guides** | | Add Composition Guides. |
| **PaperClip** | | Load your own Composition Guides. |
| **Broom** | | Clear Composition Guides. |

## Requirements

* A working installation of [ComfyUI](https://github.com/comfyanonymous/ComfyUI).

## Installation
### Step 1. Clone the Repository

First, you need to clone this repository into your `ComfyUI/custom_nodes/` directory, and install requirements.

### Step 2: Restart ComfyUI

After the repository has been successfully cloned, make sure to restart ComfyUI. This will allow it to recognize and load the new custom node.

## Credits

Original developer: Machine Delusions from the Fill-Nodes pack.

* **Original Project:** [ComfyUI\_FL-Path-Animator](https://github.com/filliptm/ComfyUI_FL-Path-Animator)  
* **Original Developer:** Machine Delusions

This version includes significant modifications and new features.
