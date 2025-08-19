# Car Damage Detection

## Dataset - Car Damage Detection by Anuj Shah
Link[https://www.kaggle.com/datasets/anujms/car-damage-detection]

- The Dataset structure:
    1. training: 
        00-damage - 920 files
        00-whole - 920 files
    2. validation:
        00-damage - 230 files
        00-whole - 230 files
    
    Total files: 2299

## Pipeline
    1. Data Preparation
        - Load data
        - Label Encoding
    2. Data Preprocessing 
        - Resize Images
        - Normalize
        - Augmentation
    3. Model
    4. Training
    5. Evaluation
myy 

### 1. Data Preparation
- Load Data: Load the images into the dataset.
- Label Encoding: Assign labels (0 for damaged & 1 for not damaged).

### 2. Data Preprocessing
- Resize Images: Scaling images to 224 X 224 pixels (ResNet Input).
- Normalize:
    - Scaling: Dividing pixel values (originally 0-255) by 255 to bring them into the 0-1 range.
    - Standardization (Mean and Standard Deviation): Subtracting the mean and dividing by the standard deviation of the dataset for each color channel. 

### 3. Data Augmentation
- Random Cropping:
    - Random Rotations: Rotating the image by a random angle.
    - Random Translations: Shifting the image horizontally or vertically.
    - Random Horizontal/Vertical Flips (Mirroring): Mirroring the image along its horizontal or vertical axis.
- Color Space Transformations:
    - Random Brightness/Contrast/Saturation Adjustments: Modifying the color properties of the image.
- Random Color Jitter: Applying random changes to the color channels.
- Grayscale Conversion: Converting color images to grayscale.