# Masked Language Model Attention Visualizer

This project leverages a pre-trained BERT model to predict missing words in a sentence and visualize the self-attention patterns within the model. The program displays the top predictions for masked tokens in the input text and generates attention diagrams for each attention layer and head, showing the importance of each token in relation to others.

## Features

- **Masked Token Prediction**: Using BERT (`bert-base-uncased`), the model predicts up to 3 possible replacements for masked tokens.
- **Attention Visualization**: Produces graphical representations of self-attention scores across all layers and heads of the model.

## Requirements

- **Python 3.x**
- **Packages**: `tensorflow`, `transformers`, `Pillow`
- **Font File**: Requires `OpenSans-Regular.ttf` font in the `assets/fonts/` directory.

## Setup

1. **Install dependencies**:
   ```bash
   pip install tensorflow transformers pillow
   ```

2. **Ensure font availability**:
   - Place the `OpenSans-Regular.ttf` font file in `assets/fonts/`.

## Usage

1. **Run the script**:
   ```bash
   python script_name.py
   ```

2. **Input Text**: When prompted, enter a sentence containing a `[MASK]` token where you want predictions.

3. **Output**:
   - **Predicted Tokens**: The top 3 predictions for the masked token are printed.
   - **Attention Visualizations**: Diagrams representing self-attention scores for each layer and head are saved as images named `Attention_LayerX_HeadY.png`.

## Code Overview

- **Main Functions**:
  - `main()`: Manages input, tokenization, and masked token prediction.
  - `get_mask_token_index()`: Finds the masked token in the tokenized input.
  - `get_color_for_attention_score()`: Converts attention scores to grayscale values.
  - `visualize_attentions()`: Generates attention diagrams for all layers and heads.
  - `generate_diagram()`: Creates and saves an individual attention diagram for a specified layer and head.

