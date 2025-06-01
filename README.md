# Cosmos-x-DocScope

Cosmos-x-DocScope is a Gradio-based application that integrates and provides an interface for interacting with three distinct vision-language models: **Cosmos-Reason1-7B**, **docscopeOCR-7B-050425-exp**, and **Captioner-Relaxed-7B**. This application allows users to perform both image and video inference, leveraging the unique capabilities of each model for tasks such as visual reasoning, optical character recognition, and detailed image captioning.

-----

## Features

  * **Image Inference:** Upload an image and provide a text query to get a response from the selected model.
  * **Video Inference:** Upload a video and provide a text query to get a summarized understanding of the video content. The video is downsampled into key frames for analysis.
  * **Multiple Models:** Choose between:
      * **Cosmos-Reason1-7B:** Designed for understanding physical common sense and generating embodied decisions.
      * **docscopeOCR-7B-050425-exp:** Optimized for document-level optical character recognition and long-context vision-language understanding.
      * **Captioner-Relaxed-7B:** Built with a hand-curated dataset for text-to-image models, providing significantly more detailed descriptions or captions of given images.
  * **Adjustable Parameters:** Fine-tune generation parameters like `Max new tokens`, `Temperature`, `Top-p`, `Top-k`, and `Repetition penalty` for customized output.
  * **Interactive Interface:** A user-friendly Gradio interface with separate tabs for image and video inputs.
  * **Examples:** Pre-defined examples to quickly test the image and video inference functionalities.

-----

## Installation

To set up and run this application, follow these steps:

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/PRITHIVSAKTHIUR/Cosmos-x-DocScope.git
    cd Cosmos-x-DocScope
    ```

2.  **Create a virtual environment (recommended):**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3.  **Install the required dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

      * Note: The `requirements.txt` file should include `gradio`, `transformers`, `torch`, `Pillow`, `numpy`, `opencv-python`, and `spaces` (if `spaces` is a specific dependency, otherwise it's typically for Hugging Face Spaces deployment).

-----

## Usage

To launch the Gradio application, run the following command from the project's root directory:

```bash
python app.py
```

(Assuming your main application file is named `app.py` from the provided code snippet.)

Once the application is running, open the provided local URL (e.g., `http://127.0.0.1:7860`) in your web browser.

### Interface Overview

  * **Query Input:** Enter your text query for the model.
  * **Image/Video Upload:** Upload your image or video file.
  * **Submit Button:** Click to initiate the generation process.
  * **Output:** The model's generated response will appear here.
  * **Select Model:** Choose which of the three models you want to use.
  * **Advanced options:** Expand this section to adjust generation parameters.

-----

## Model Information

  * **Cosmos-Reason1-7B:**

      * Hugging Face Model Card: [nvidia/Cosmos-Reason1-7B](https://huggingface.co/nvidia/Cosmos-Reason1-7B)
      * **Purpose:** Specializes in understanding physical common sense and generating appropriate embodied decisions.

  * **docscopeOCR-7B-050425-exp:**

      * Hugging Face Model Card: [prithivMLmods/docscopeOCR-7B-050425-exp](https://huggingface.co/prithivMLmods/docscopeOCR-7B-050425-exp)
      * **Purpose:** Optimized for document-level optical character recognition (OCR) and long-context vision-language understanding, making it suitable for analyzing complex documents.

  * **Captioner-Relaxed-7B:**

      * Hugging Face Model Card: [Ertugrul/Qwen2.5-VL-7B-Captioner-Relaxed](https://huggingface.co/Ertugrul/Qwen2.5-VL-7B-Captioner-Relaxed)
      * **Purpose:** Designed to provide significantly more detailed descriptions or captions of given images, often built with hand-curated datasets for text-to-image models.
