# Image Captioning with Deep Learning

An end-to-end image captioning system using the Flickr8k dataset with an encoder-decoder architecture implemented in TensorFlow/Keras.

## Project Overview
This project implements an image captioning system that generates textual descriptions for images by combining computer vision and natural language processing techniques. The model uses a pre-trained CNN (InceptionV3) as an encoder to extract image features and an LSTM-based decoder to generate captions.

## Dataset
The model is trained on the Flickr8k dataset, containing 8,091 images with 5 captions each.

## Model Architecture
- **Encoder**: Pre-trained InceptionV3 CNN (excluding classification layer)
- **Decoder**: LSTM-based language model with embedding layer

## Requirements
See requirements.txt file.

## Setup and Usage
1. Create virtual environment: `python -m venv image_captioning_env`
2. Activate environment:
   - Windows: `image_captioning_env\Scripts\activate`
   - macOS/Linux: `source image_captioning_env/bin/activate`
3. Install requirements: `pip install -r requirements.txt`
4. Download Flickr8k dataset and update paths in the notebook
5. Run notebook cells sequentially

## Results
The model generates image captions using both greedy search and beam search algorithms, and is evaluated using BLEU scores.

## Directory Structure
- `image_captioning.ipynb`: Main Jupyter notebook with all code
- After running the notebook:
  - `processed_data/`: Preprocessed captions and vocabulary files
  - `models/`: Saved model checkpoints
  - `features_dir/`: Extracted image features