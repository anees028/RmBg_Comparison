# Background Removal Application

This application uses the `rembg` library to remove backgrounds from images. It provides a simple and efficient way to process images and remove their backgrounds using deep learning models.

## Features

- Remove backgrounds from images with high accuracy
- Support for various image formats (JPEG, PNG, etc.)
- Simple and easy-to-use interface
- GPU acceleration support for faster processing
- Includes sample test images for immediate testing

## Prerequisites

- Python 3.x
- pip (Python package installer)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/RemBg_python_app.git
cd RemBg_python_app
```

2. Install the required dependencies:
```bash
pip install rembg
pip install onnxruntime
```

## Usage

### Test Images

The repository includes sample images for testing:
- `car-input.jpg`: Sample input image with a car
- `car-output.png`: Example output after background removal

You can use these images to test the application immediately after installation.

### As a Library

```python
from rembg import remove
from PIL import Image

# Load the image
input_image = Image.open('car-input.jpg')  # Using the provided test image

# Remove the background
output_image = remove(input_image)

# Save the result
output_image.save('output.png')
```

### Using Jupyter Notebook

1. Open the `RemBg_app.ipynb` notebook
2. The notebook includes examples using the provided test images
3. Follow the cells to process your images
4. The notebook provides examples for both single image and batch processing

## How It Works

The application uses the `rembg` library, which implements a deep learning model to detect and remove backgrounds from images. The process involves:

1. Loading the input image
2. Processing the image through the neural network
3. Generating a new image with the background removed
4. Saving the result with transparency

## Supported Image Formats

- JPEG/JPG
- PNG
- Other common image formats supported by PIL

## Performance

- The application can utilize GPU acceleration for faster processing
- Processing time depends on the image size and your hardware configuration

## Contributing

Feel free to submit issues and enhancement requests!

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [rembg](https://github.com/danielgatis/rembg) - The core library used for background removal
- [PIL (Python Imaging Library)](https://python-pillow.org/) - For image processing
