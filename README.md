# Detection of Hateful Memes using Multimodal AI

This repository contains the source code for a machine learning model designed to detect hateful content in memes. The model uses a multimodal approach, analyzing both the image content and the extracted text to make a more accurate and context-aware classification.



### 🧠 Motivation & Problem Statement

The spread of hateful content online is a significant challenge, and memes represent a particularly difficult case. Their meaning is often derived from a complex interplay between the image and the text, a concept known as multimodality. A text-only filter might miss hate speech in an image, and an image-only filter would not understand the text's context.

Before building this model, I conducted research into existing academic work on multimodal hate speech detection, reviewing papers from sources like Google Scholar. This research confirmed that state-of-the-art results are achieved by systems that process both data streams (vision and language) simultaneously. This project is a practical implementation of those findings, aiming to build a more effective classifier.

---

### 🛠️ Tech Stack

- **Backend & Model:** Python
- **ML Libraries:** TensorFlow/PyTorch, Scikit-learn
- **Computer Vision:** OpenCV
- **Text Processing:** Tesseract (for OCR), NLTK / Hugging Face Transformers
- **Environment:** Jupyter Notebook

---

### ✨ Key Features

- **Optical Character Recognition (OCR):** Extracts embedded text from meme images.
- **Image Analysis:** Processes the visual components of the meme to understand its context.
- **Text Analysis:** Analyzes the sentiment and meaning of the extracted text.
- **Multimodal Classification:** Combines image and text features to make a final prediction (Hateful / Not Hateful).
- Achieved **91% accuracy** on the test set from the Facebook Hateful Memes dataset.

---

### 🚀 Setup and Installation

To get this project running locally, follow these steps:

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/ashmitasenroy/Detection-of-Hateful-Memes.git
    ```

2.  **Navigate into the directory:**
    ```sh
    cd Detection-of-Hateful-Memes
    ```

3.  **Install the required dependencies:**
    *(Note: You must have a `requirements.txt` file in your repo for this to work. You can generate one with `pip freeze > requirements.txt`)*
    ```sh
    pip install -r requirements.txt
    ```

---

### 🏃‍♀️ How to Use

To run a prediction on a new meme image, use the `predict.py` script:

```sh
python predict.py --image path/to/your/image.jpg
