# DCGANs for Cat Image Generation

This repository contains the implementation of a Deep Convolutional Generative Adversarial Network (DCGAN) for generating realistic cat images. This project was conducted as part of an individual research project at KAIST. 

The link to access the notebook is https://colab.research.google.com/drive/1rXnMAYlmY6gmqJCQ8JDWoR9QLy4Tr3oR?usp=sharing as GitHub forbids the upload of large sized files.

The link to access the individual research report is https://drive.google.com/file/d/1ot4O_ypvOf6aJKUpXuexmL8cAatp8aIP/view?usp=sharing.

## Project Overview
The objective of this project was to explore generative adversarial networks (GANs) and their application to image synthesis. Using the DCGAN architecture, the model was trained on a dataset of cat images to generate new, realistic cat images.

## Dataset
The dataset used for training is the [Hugging Face HugGAN Cats Dataset](https://huggingface.co/datasets/huggan/cats). It contains a variety of cat images preprocessed to 64x64 resolution.

## Model Architecture
The DCGAN model follows the standard architecture outlined by Radford et al. (2015):
- Generator: A series of transposed convolutional layers, batch normalization, and ReLU activations to generate 64x64 RGB images.
- Discriminator: A series of convolutional layers, batch normalization, and LeakyReLU activations to classify images as real or fake.

## Installation
To set up the environment and install required packages, run the following commands:

```bash
# Create a virtual environment (optional but recommended)
python -m venv dcgan_env
source dcgan_env/bin/activate  # On Windows, use: .\dcgan_env\Scripts\activate

# Install required packages
pip install -r requirements.txt
```

## Training the Model
To train the DCGAN model, execute the following command:

```bash
python train_dcgan.py --dataroot <path_to_dataset> --batch_size 64 --epochs 100
```

Adjust hyperparameters such as `batch_size` and `epochs` according to your system's capacity.

## Generating Images
After training, you can generate cat images using the trained generator:

```bash
python generate_images.py --num_images 10
```

Generated images will be saved in the `output` directory.

## Results
Here are some sample images generated by the DCGAN model:

![Generated Cat Images](output/sample_generated_images.png)

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- The Hugging Face team for providing the cat image dataset.
- KAIST for supporting this individual research project.
