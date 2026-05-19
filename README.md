# 🏏 Clode X Blender – Realistic 3D Cricket Stadium Generator

> **Generate a fully textured, colorful cricket stadium in Blender with a single Python script.**  
> No external assets, no heavy modelling – just pure code.

![Blender Version](https://img.shields.io/badge/Blender-3.0+-orange?logo=blender)
![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📖 Overview

**Clode X Blender** is a standalone Blender Python script that creates a **complete, realistic cricket stadium** from scratch using only primitive shapes and procedural materials. The stadium includes:

- A full cricket pitch with stumps, bails, and creases  
- Multi‑tier stands with **colorful seat sections**  
- Boundary rope, flags, sight screens, and advertisement boards  
- Floodlight towers with dynamic lights  
- A pavilion building, scoreboard, and player dugouts  
- **Thousands of instanced crowd figures** with random shirt colors  
- Pre‑placed cameras and a sun‑lit environment  

All objects are generated procedurally – **no external textures, no manual modelling**. Perfect for animations, VR walkthroughs, or simply exploring a digital cricket ground.

---

## 🚀 Features

- ✅ **One‑click generation** – run the script and the stadium appears instantly  
- ✅ **Real‑world scale** – pitch length 20.12 m, boundary radius ~75 m  
- ✅ **Colorful & vibrant** – rainbow crowd, bright seat sections, team‑colored dugouts  
- ✅ **Optimised performance** – instancing, arrays, and low‑poly meshes keep the scene light  
- ✅ **Ready to render** – Cycles materials, sky texture, and cameras are pre‑configured  
- ✅ **No external dependencies** – uses only Blender’s built‑in Python API  

---

## 📦 Requirements

| Software | Minimum Version |
|----------|----------------|
| [Blender](https://www.blender.org/) | 3.0 or later (3.6 LTS recommended) |
| RAM | 4 GB (8 GB recommended for crowd) |
| GPU | Any OpenGL 3.3+ compatible |

> The script works on **Windows, macOS, and Linux**.

---

## 🛠️ Installation & Usage

### 1. Download the script

Copy the script from `cricket_stadium.py` (provided in this repository) to your local machine.

### 2. Open Blender

Launch Blender and switch to the **Scripting** workspace (top bar → `Scripting`).

### 3. Paste & Run

- Paste the entire script into the text editor.
- Press **`Alt + P`** or click the **Run Script** button (▶️).

### 4. Watch the magic happen

The script will print progress messages in the console. After 10–30 seconds, you’ll see:


### 5. Navigate & Render

| Action | Shortcut |
|--------|----------|
| Rotate view | Middle mouse button |
| Pan | Shift + middle mouse |
| Zoom | Scroll wheel |
| Overview camera | Numpad 0 |
| Render image | F12 |
| Switch to material preview | Z → Material Preview |

---

## 🎮 Controls (Viewport)

No special add‑on required – use Blender’s native navigation:

- **W/A/S/D** – only works if you enable "Walk Navigation" (`Shift + ~` then `W/A/S/D`).  
- Or simply orbit, pan, and zoom freely.

> For a first‑person walk on the pitch, press `Shift + ~`, then use `W/A/S/D` and mouse to look around.

---

## 📂 Project Structure

---

## 🧠 How It Works

The script uses Blender’s `bpy` module to:

1. **Clear the scene** – removes default cube, camera, and light.
2. **Build geometry** – creates planes, cylinders, and cubes for the field, stands, and buildings.
3. **Apply materials** – procedural shaders (noise, mixRGB, sky texture) for grass, pitch, seats, etc.
4. **Instance objects** – crowd figures are duplicated from a single low‑poly template.
5. **Add lighting** – sun lamps, fill lights, and floodlight point lights.
6. **Place cameras** – sets up several useful camera positions.

Everything is grouped in a collection named **`Cricket_Stadium`** for easy management.

---

## 🎨 Customisation Ideas

Want to tweak the stadium? Modify the script variables:

| Variable | Location | Effect |
|----------|----------|--------|
| `MAX = 3000` | `add_crowd()` | Lower for faster generation / higher for denser crowd |
| `shirt_colors` | `add_crowd()` | Change crowd jersey colors |
| `sections` | `build_stands()` | Modify seat section angles and colors |
| `tower_angles` | `create_floodlights()` | Reposition light towers |
| `scene.cycles.samples` | `setup_lighting()` | Adjust render quality |

> Always save your changes as a new `.py` file before re‑running.

---

## 📸 Screenshots

Watch the stadium come to life – from script execution to interactive walkthrough.

![Img1](https://github.com/1khalaneshubham/Clode_X_Blender/blob/main/img1.png)
![Img2](https://github.com/1khalaneshubham/Clode_X_Blender/blob/main/img2.png)
![Img3](https://github.com/1khalaneshubham/Clode_X_Blender/blob/main/img3.png)
![Img4](https://github.com/1khalaneshubham/Clode_X_Blender/blob/main/img4.png)
![Img5](https://github.com/1khalaneshubham/Clode_X_Blender/blob/main/img5.png)

---

## 🤝 Contributing

Contributions are welcome! If you have ideas for improvements:

- Fork the repository.
- Create a new branch (`git checkout -b feature/amazing-idea`).
- Commit your changes (`git commit -m 'Add amazing feature'`).
- Push to the branch (`git push origin feature/amazing-idea`).
- Open a Pull Request.

Please ensure your code follows the existing style (clear functions, comments, and no external file dependencies).

---

## ❓ Troubleshooting

| Issue | Solution |
|-------|----------|
| **Script runs slowly** | Lower `MAX` crowd count (e.g., 1500). Also reduce `vertices` on circle primitives. |
| **Stands or crowd not visible** | Switch viewport shading to **Material Preview** or **Rendered**. |
| **No lights after generation** | Ensure you are in `Cycles` or `Eevee` render engine. The script sets `CYCLES` by default. |
| **Error: `'World' object has no attribute 'node_tree'`** | Re‑run the script – this rarely happens. If persistent, comment out the sky texture section. |
| **Can't run script** | Make sure you are in Blender’s **Scripting** workspace and press `Alt + P`. |

---

## 📜 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- Built with [Blender Python API](https://docs.blender.org/api/current/)
- Inspired by real cricket stadiums (MCG, Lord’s, Eden Gardens)
- Thanks to the Blender community for endless learning resources

---

## 📬 Contact

For questions or suggestions, please open an [Issue](https://github.com/yourusername/Clode-X-Blender/issues) on GitHub.

---

**Enjoy your virtual cricket stadium!** 🏏✨  
*Generated entirely in Blender – no CAD, no external textures, just Python.*

