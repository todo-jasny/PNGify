# PNG Image Handler

## Description
This Python project allows for the creation, reading, and manipulation of PNG images, specifically providing a way to:

- Create PNG images from RGBA pixel data.
- Read PNG images and extract RGBA pixel data.
- Resize PNG images while maintaining their aspect ratio.

The main functionality is implemented via two classes: `PNGCcreator` for creating PNG images and `PNGReader` for reading and extracting pixel data from PNG images. Additionally, a function to resize PNG images is provided.

## Features

- **PNG Creation**: Generate PNG files from raw RGBA pixel data.
- **PNG Reading**: Read and extract pixel data from PNG files.
- **PNG Resizing**: Resize PNG images while preserving the image data and quality.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/png-image-handler.git
   cd png-image-handler

2. Install with pip
   ```bash
   pip install .

3. Install dependencies:
This project uses standard Python libraries such as struct, zlib, and os, which come pre-installed with Python, so no external dependencies are required.

## Usage
**Creating a PNG Image**
To create a PNG image using the PNGCcreator class:

   ```bash
   from png_creator import PNGCreator

   # Define image dimensions and RGBA pixel data
   width = 256
   height = 256
   pixel_colors = [(255, 0, 0, 255) for _ in range(width * height)]  # Red image for example

   # Create a PNG creator object and save the image
   png_creator = PNGCreator(width, height, pixel_colors)
   png_creator.save('output_image.png')
   ```

**Reading a PNG Image**
To read a PNG image and extract RGBA pixel data using the PNGReader class:

```python
from png_reader import PNGReader

# Define the path to the PNG file
file_path = 'output_image.png'

# Create a PNG reader object and read the image
png_reader = PNGReader(file_path)
png_reader.read()

# Access the RGBA pixel data
rgba_pixels = png_reader.rgb_tuples
```

**Resizing a PNG Image**
To resize a PNG image to a new width and height:

```python
from resize import resize_png

# Resize the image to the new dimensions
resize_png('output_image.png', 1000, 1000)
This will create a resized version of the image with the dimensions 1000x1000 while preserving the image data.
```

Contributing
Feel free to fork this project, submit issues, or open pull requests. Contributions are welcome!

License
This project is licensed under the MIT License.






