# 🎨 Neural Style Transfer

A **Deep Learning-based Neural Style Transfer** web application built with **Python, PyTorch, and Flask**. The application allows users to combine the content of one image with the artistic style of another image to generate a new stylized image.

The project uses a trained neural network model to perform image style transfer and provides a simple web interface through Flask.

---

## 📌 Project Overview

Neural Style Transfer is a deep learning technique that combines two images:

* **Content Image** — The image whose structure/content you want to preserve.
* **Style Image** — The image whose artistic appearance you want to apply.

The model generates a new image that preserves the semantic content of the content image while adopting the visual characteristics of the style image.

### Example

```text
Content Image + Style Image
           ↓
    Neural Style Transfer
           ↓
      Stylized Image
```

---

## ✨ Features

* 🎨 Transfer artistic styles between images
* 🖼️ Upload content and style images
* 🧠 Deep learning-based image transformation
* ⚡ PyTorch-based inference
* 🌐 Flask web application
* 📁 Image upload and processing
* 💾 Generated image output
* 💻 Supports CPU inference
* 📦 Pre-trained decoder model included

---

## 🛠️ Technologies Used

| Technology          | Purpose                           |
| ------------------- | --------------------------------- |
| **Python**          | Core programming language         |
| **PyTorch**         | Deep learning and model inference |
| **Flask**           | Backend web framework             |
| **Flask-WTF**       | Form handling and validation      |
| **WTForms**         | File upload forms                 |
| **Flask-Bootstrap** | Web UI styling                    |
| **Pillow**          | Image processing                  |
| **NumPy**           | Numerical operations              |
| **Torchvision**     | Computer vision utilities         |

---

## 🧠 How Neural Style Transfer Works

The system takes two input images:

### 1. Content Image

The content image provides the structure and semantic information that should be preserved.

### 2. Style Image

The style image provides artistic characteristics such as:

* Colors
* Textures
* Patterns
* Brush strokes
* Visual appearance

### 3. Feature Extraction

A deep convolutional neural network extracts meaningful visual representations from the images.

### 4. Adaptive Instance Normalization

The AdaIN approach aligns the feature statistics of the content representation with those of the style representation.

Conceptually:

```text
Content Image
      ↓
Feature Extraction
      ↓
Content Features ──────┐
                       │
Style Image             │
      ↓                 │
Feature Extraction      │
      ↓                 │
Style Features ─────────┤
                       ↓
             Adaptive Instance
                Normalization
                       ↓
                  Decoder
                       ↓
              Stylized Image
```

### 5. Decoder

The trained decoder reconstructs the stylized image from the transformed feature representation.


---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/Princy0605/Neural_Style_Transfer.git
```

Navigate into the project:

```bash
cd Neural_Style_Transfer
```

---

### 2. Create a virtual environment

It is recommended to use **Python 3.11**.

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```powershell
.\venv\Scripts\Activate
```

---

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

The project uses PyTorch, Flask, Flask-WTF, Pillow, NumPy, and other required dependencies.

---

## 🚀 Running the Application

Navigate to the Flask application directory:

```bash
cd NST_Code
```

Start the Flask application:

```bash
python app.py
```

The application will start on the local Flask server.

Open your browser and visit:

```text
http://localhost:5000
```

---

## 🖥️ Usage

1. Start the Flask application.
2. Open the application in your browser.
3. Upload a **content image**.
4. Upload a **style image**.
5. Submit the images for processing.
6. The neural style transfer model processes the images.
7. The generated stylized image is displayed.
8. Save the resulting image locally.

---

## 🤖 Model

The project uses a trained PyTorch decoder:

```text
experiment/final_exp/decoder_final.pth
```

The decoder is loaded during application startup and is used to reconstruct the stylized image after the feature transformation.

### CPU Support

The model can be loaded on a CPU using:

```python
torch.load(decoder_path, map_location='cpu')
```

If a CUDA-compatible GPU is available, inference can be adapted to use GPU acceleration.

---

## 📋 Requirements

The project requires:

```text
Flask
Flask-Bootstrap
Flask-WTF
NumPy
Pillow
PyTorch
Torchvision
tqdm
Werkzeug
WTForms
Gunicorn
```

Install them using:

```bash
pip install -r requirements.txt
```

---

## 🎯 Applications

Neural Style Transfer can be used for:

* 🎨 Digital art generation
* 📸 Artistic photo transformation
* 🖼️ Creative image editing
* 🎭 Visual effects
* 🎨 Automated artistic rendering
* 🧠 Computer vision research
* 📚 Deep learning experimentation

---

## 🔮 Future Improvements

Possible improvements include:

* [ ] Add multiple pre-trained artistic styles
* [ ] Allow users to control style intensity
* [ ] Add image preview before processing
* [ ] Improve UI/UX
* [ ] Add support for higher-resolution images

---

## 🧪 Deep Learning Concepts

This project demonstrates practical applications of:

* Convolutional Neural Networks (CNNs)
* Deep Feature Extraction
* Image Representation
* Feature Statistics
* Adaptive Instance Normalization (AdaIN)
* Neural Style Transfer
* PyTorch Model Inference
* Computer Vision

---

## 👩‍💻 Author

**Princy Jain**

GitHub:
https://github.com/Princy0605


---

## 📄 License

This project is intended for educational and research purposes.
