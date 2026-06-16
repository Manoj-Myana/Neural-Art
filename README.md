# Neural Art 🎨

Neural Art is a web-based Neural Style Transfer application built using **PyTorch** and **Flask**. The application uses **Adaptive Instance Normalization (AdaIN)** to transfer the artistic style of one image onto another while preserving the original content.

## 🌐 Live Demo

**Deployed Application:** https://neural-art-2.onrender.com/

Try the application directly from the browser by uploading a content image and a style image.

---

## ✨ Features

* Upload Content and Style Images
* Neural Style Transfer using AdaIN
* Adjustable Style Strength (Alpha)
* Interactive Web Interface
* Fast Image Processing with PyTorch
* Real-time Stylized Image Generation
* Responsive and User-Friendly Design

---

## 📸 Sample Workflow

1. Upload a **Content Image**
2. Upload a **Style Image**
3. Adjust the **Alpha Value** (Style Intensity)
4. Click **Transfer Style**
5. Download or view the generated stylized image

---

## 🏗️ Project Structure

```text
Neural-Art/
│
├── app.py
├── train.py
├── requirements.txt
├── runtime.txt
├── vgg_normalised.pth
│
├── templates/
│   └── index.html
│
├── static/
│   └── uploads/
│
├── utils/
│   ├── models.py
│   └── utils.py
│
├── examples/
│
├── content_data/
├── style_data/
│
└── experiment/
    └── final_exp/
        └── decoder_final.pth
```

---

## 🧠 How It Works

The application follows the Adaptive Instance Normalization pipeline:

1. Content image is passed through a pretrained VGG Encoder.
2. Style image is passed through the same VGG Encoder.
3. AdaIN aligns content feature statistics with style feature statistics.
4. A trained Decoder reconstructs the stylized image.
5. The final image is displayed to the user.

---

## ⚙️ Technologies Used

### Frontend

* HTML5
* CSS3
* Bootstrap

### Backend

* Flask
* Flask-WTF

### Deep Learning

* PyTorch
* Torchvision

### Image Processing

* Pillow (PIL)

---

## 🚀 Installation

### Clone the Repository

```bash
git clone https://github.com/Manoj-Myana/Neural-Art.git
cd Neural-Art
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Running Locally

Start the Flask application:

```bash
python app.py
```

Open your browser and visit:

```text
http://localhost:5000
```

---

## 🏋️ Training the Model

Place content images inside:

```text
content_data/
```

Place style images inside:

```text
style_data/
```

Run training:

```bash
python train.py
```

Generated checkpoints will be saved inside:

```text
experiment/
```

---

## 📦 Model Files

The project uses:

* `vgg_normalised.pth` (Pretrained VGG Encoder)
* `decoder_final.pth` (Trained Decoder Network)

These files are required for inference and deployment.

---

## 🌍 Deployment

The application is deployed on **Render**.

Live URL:

https://neural-art-2.onrender.com/

Deployment Stack:

* Render Web Service
* Python 3.12
* Gunicorn
* Flask
* PyTorch

---

## 📈 Future Enhancements

* Multiple Style Blending
* Real-Time Webcam Style Transfer
* Video Style Transfer
* User Authentication
* Image Download Feature
* Cloud Storage Integration
* GPU-Based Inference

---

## 👨‍💻 Author

### Manoj Kumar

Computer Science & Engineering (Data Science)

Vignana Bharathi Institute of Technology, Hyderabad

GitHub: https://github.com/Manoj-Myana

---

## ⭐ Support

If you found this project useful, consider giving the repository a star ⭐ on GitHub.
