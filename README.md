# -YOLO-Diffusion-Image-Editing

# 🎨 Text-Guided Image Editing with Automatic Object Preservation using YOLO and Diffusion Models

An end-to-end computer vision pipeline for **text-guided image editing** while **automatically preserving selected objects** using **YOLO object detection** and **diffusion-based generative models**.

This project combines object detection and image generation to modify images according to a text prompt while protecting important objects from unintended changes.

---

# 📌 Project Overview

Traditional text-to-image editing models often modify the entire image, including objects that should remain unchanged.

This project addresses this limitation by automatically detecting objects with **YOLO**, generating preservation masks, and applying a diffusion model only to editable regions.

The result is a more controllable image editing pipeline that preserves the semantic integrity of important objects.

Before                After

<p align="center">

<img src="data/inputs/test.jpeg" width="23%">

<img src="data/outputs/detections/person_mask2.png" width="23%">

<img src="data/outputs/detections/person_cutout.png" width="23%">

<img src="data/outputs/generated_background.png" width="23%">

</p>

---

# 🚀 Features

- ✅ Automatic object detection using YOLO
- ✅ Automatic object preservation mask generation
- ✅ Text-guided image editing
- ✅ Diffusion-based image generation
- ✅ Editable region masking
- ✅ High-quality image synthesis
- ✅ Modular pipeline
- ✅ Easy customization

---

# 🧠 Pipeline

```text
                  Input Image
                       │
                       ▼
              YOLO Object Detection
                       │
                       ▼
            Object Preservation Mask
                       │
                       ▼
               Text Prompt Input
                       │
                       ▼
          Diffusion Image Editing
                       │
                       ▼
             Edited Image Output
```

---

# ⚙️ Methodology

The proposed framework consists of the following stages:

### 1. Object Detection

YOLO detects important objects in the input image.

---

### 2. Mask Generation

Detected bounding boxes are converted into preservation masks.

These regions remain unchanged during editing.

---

### 3. Text-Guided Editing

A diffusion model receives:

- Original image
- Preservation mask
- Text prompt

and generates an edited image.

---

### 4. Image Reconstruction

Protected regions are merged with generated regions to produce the final image.

---

# 🛠 Technologies

- Python
- PyTorch
- Ultralytics YOLO
- Diffusers
- Hugging Face Transformers
- OpenCV
- Pillow
- NumPy
- Matplotlib

---

# 📦 Installation

Clone the repository

```bash
git clone https://github.com/roghayefazli/text-guided-image-editing.git

cd text-guided-image-editing
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Usage

1. Load an input image

2. Detect objects using YOLO

3. Generate preservation masks

4. Enter a text prompt

Example:

```
Replace the sky with a sunset while keeping the people unchanged.
```

5. Generate the edited image

---

# 📊 Example Workflow

```
Input Image
      │
      ▼
YOLO Detection
      │
      ▼
Mask Generation
      │
      ▼
Stable Diffusion
      │
      ▼
Edited Image
```

---

# 🔬 Future Improvements

- Segment Anything (SAM) integration
- Multi-object preservation
- Real-time editing
- Interactive object selection
- Inpainting refinement
- Support for multiple diffusion models (SDXL, FLUX)

---

# 👩‍💻 Author

**Roghayeh Fazli**

GitHub: https://github.com/roghayefazli
