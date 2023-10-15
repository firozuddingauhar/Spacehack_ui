# Antriksh Arcane Assistant

Antriksh Arcane Assistant is an AI-powered software designed to assist astronauts in overcoming problems that may occur during space missions. This software takes two inputs: the items available and the specific problem that has arisen. It leverages a fine-tuned AI model trained on space-related data, including astrophysics, spaceship designs, and manuals, to provide valuable solutions and safety measures.

![Antriksh Arcane Assistant](screenshot.png)

## Features

- **AI Assistance:** Provides real-time assistance to astronauts facing challenges during space missions.

- **Fine-Tuned Model:** The AI model used in this software is fine-tuned on space-related data, making it highly specialized for space missions.

- **Problem-Specific Solutions:** Offers tailored solutions based on the given problem and available resources.

- **User-Friendly Interface:** The user interface is designed for ease of use and quick access to assistance.

## Requirements

To run Antriksh Arcane Assistant, you need the following:

- Python (version 3.x recommended)
- Required Python packages (install using `pip install -r requirements.txt`):
  - Kivy
  - Transformers
  - KivyMD
  - Pandas
  - Numpy

## Model Training

The AI model used in this project is fine-tuned on space-related data. Here's how you can train the model:

1. Create a text file (e.g., `train.txt`) and populate it with space-related data, including astrophysics information, spaceship designs, and manuals.

2. Run the training script present in backend to fine-tune the GPT-2 model:

   ```bash
   python model_implementation.py
   ```

   - `train_file_path`: Path to the training data file (e.g., `train.txt`).
   - `model_name`: Pretrained model name (e.g., 'gpt2').
   - `output_dir`: Output directory for saving the fine-tuned model.
   - `overwrite_output_dir`: Set to `True` to overwrite the output directory if it exists.
   - `per_device_train_batch_size`: Batch size for training.
   - `num_train_epochs`: Number of training epochs.
   - `save_steps`: Number of steps before saving the model.

3. Once training is complete, the fine-tuned model and tokenizer will be saved in the specified output directory (`./custom_model` by default).

## Usage

1. Run the Antriksh Arcane Assistant application using the following command:

   ```bash
   python main.py
   ```

2. The application opens with two input fields: "Items Present" and "Problem Occurred."

3. Enter the items available to the astronaut and describe the problem they are facing.

4. Click the "Send" button to submit the problem to the AI assistant.

5. The AI assistant will provide a response with solutions and safety measures tailored to the problem and available items.

## About the Model

The AI model used in this project is based on the GPT-2 architecture, fine-tuned on space-related data to provide context-aware responses. It generates solutions based on the astronaut's input and the provided context.

## Author

This project was developed by [Hammad Ali](https://github.com/hammadali1805).
