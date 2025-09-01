# Road Following + Collision Avoidance on JetBot

## 🧠 Introduction

This project integrates **road following** and **collision avoidance** into a single pipeline using NVIDIA JetBot. Leveraging optimized deep learning models via TensorRT, the bot can autonomously navigate paths while avoiding real-time obstacles.

The notebook combines a regression model (for road following) and a classification model (for collision detection), enabling robust autonomous navigation on JetBot.

---

## 📑 Table of Contents

- [Introduction](#-introduction)
- [Installation](#-installation)
- [Usage](#-usage)
- [Features](#-features)
- [Dependencies](#-dependencies)
- [Configuration](#-configuration)
- [Examples](#-examples)
- [Troubleshooting](#-troubleshooting)
- [Contributors](#-contributors)
- [License](#-license)

---

## 💾 Installation

1. Clone this repository or download the notebook:
   ```bash
   git clone <repository-url>
   ```

2. Install required Python packages (preferably in a Jetson Nano environment):
   ```bash
   pip install torch torchvision jetbot ipywidgets traitlets
   ```

3. Upload the following model files into the same directory as the notebook:
   - `best_steering_model_xy_trt.pth` – for road following
   - `best_model_trt.pth` – for collision avoidance

---

## 🚀 Usage

1. Power on the JetBot and launch Jupyter Notebook.
2. Open `RoadFollowing+CollisionAvoidance.ipynb`.
3. Run each cell sequentially to:
   - Load the TensorRT models.
   - Start the camera feed.
   - Preprocess the input.
   - Perform real-time steering and obstacle avoidance.
4. The JetBot should now follow the road and avoid any collisions autonomously.

---

## ✨ Features

- 🛣️ **Road Following** using regression model output (`x`, `y` steering).
- 🧱 **Collision Avoidance** using classification model (`blocked` or `free`).
- ⚡ Optimized with **TensorRT** for fast inference on Jetson Nano.
- 🎥 Real-time camera feed with live inference.

---

## 📦 Dependencies

- Python 3.6+
- `torch`
- `torchvision`
- `torch2trt`
- `jetbot`
- `ipywidgets`
- `traitlets`
- `cv2`
- `PIL`
- `numpy`

---

## ⚙️ Configuration

- Image dimensions: `224x224`
- FPS: `10`
- Model input normalization using:
  - Mean: `[0.485, 0.456, 0.406]`
  - Std: `[0.229, 0.224, 0.225]`
- Models must be converted to TensorRT format (`.pth`) before use.

---

## 🧪 Examples

To be added — you can share example images or short video/GIFs showing JetBot navigating a track and avoiding obstacles.

---

## 🛠️ Troubleshooting

- **Model Not Found**: Ensure `.pth` model files are in the same directory as the notebook.
- **Camera Not Working**: Restart the notebook or check camera initialization code.
- **JetBot Not Moving**: Check motor calibration and ensure it's on a flat surface.

---

## 👨‍💻 Contributors

Add your name or usernames here, for example:

- [Your Name](https://github.com/yourusername)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
