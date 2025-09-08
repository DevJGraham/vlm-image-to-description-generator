# vlm-image-to-description-generator

## Overview
Pipeline that takes auction images and generates a working description for an online auction website. Vision signals (labels, objects, OCR text) can be combined with a VLM to produce richer, more accurate item descriptions.

## Tools used
- Google Cloud Storage (GCS) for image hosting
- Google Cloud Vision API for labels, objects, and OCR
- Python + Jupyter/Colab as the runtime
- Hugging Face Transformers (JoyCaption/LLaVA) for captioning
- Pillow (PIL) for basic image handling

## Structure of Code
- `google_vision_api.ipynb`: Reads images from GCS and generates **labels**, **objects**, and **text/OCR** that will be passed to the JoyCaption model to assist description writing.
- `llama_joy_caption.ipynb`: Generates a description from the first thumbnail image (will optionally use Vision outputs to improve accuracy).

## Future Work
- Combine the two notebooks into one full pipeline (`full_pipeline.ipynb`).
- Allow users to provide a manifest (CSV/JSON) of items; the pipeline will parse and process every image.

If you want to contribute or have any questions, reach out.
