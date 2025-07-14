# Water - Land Segmentation using Unet++

The goal of this project is to perform semantic segmentation on satellite imagery
to differentiate between water bodies and land regions, which is crucial for environmental
monitoring, urban planning, and disaster response.

## Dataset Information
- Source of dataset: [Kaggle – DeepGlobe Land Cover Classification Dataset.](https://www.kaggle.com/datasets/balraj98/deepglobe-land-cover-classification-dataset)
- The dataset came pre-annotated with pixel-wise class labels.
- Dataset size: 803 images, 7 land cover classes (Urban, Agriculture, Rangeland, Forest, Water,
Barren, Unknown)
    - Training set size: 481 ≈ 59.90%
    - Validation set size: 121 ≈ 15.07%
    - Testing set size: 201 ≈ 25.03%

- Data augmentation applied:
Resize to 320×320, Horizontal and vertical flips, Random brightness and contrast adjustments

## Features

- Data loading and preprocessing for satellite images
- Visualization of input data and results
- Model training for land cover classification
- Evaluation metrics and analysis
- Export of predictions and results

## AI Model Used
- `U-Net++`. Model is pre-trained, I fine-tuned. `timm-regnety_120` encoder pre-trained
on ImageNet.
## Training Process and Hyperparameters
- Frameworks: PyTorch Lightning and PyTorch
- Training duration: 15 Epoch with early stopping
- Number of epochs: Max 15
- Batch size: 5
- Learning rate: 0.0001
- Optimizer used: AdamW
- GUI: Gradio

## Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/landCover.git
    cd landCover
    ```

2. Launch Jupyter Notebook:
    ```bash
    jupyter notebook land_cover.ipynb
    ```

3. Follow the notebook cells to:
    - Load and preprocess data
    - Train and evaluate models
    - Visualize results

## Colab
[https://colab.research.google.com](https://colab.research.google.com/drive/1HQot5n0loAhACqEbtfOHOye_QwyyMFvZ#scrollTo=WxYmTV5fpQrJ)


## Results

```bash
    'test/Loss': 0.4037170708179474,
    'test/IoU': 0.7059532403945923,
    'test/Accuracy': 0.9458420276641846,
    'test/Precision': 0.8104460835456848,
    'test/Recall': 0.8104460835456848,
    'test/F1score': 0.8104460835456848
```


## Contributing

Pull requests and issues are welcome. Please follow the code style and add tests where possible.

## License

This project is licensed under the `MIT License`
.
