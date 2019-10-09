# Cropyble

**Author**: Skyler Burger
**Version**: 1.1.4

## Overview
Cropyble is a class that allows a user to easily perform crops on an image containing recognizable text. This class utilizes optical character recognition (OCR) with the assitance of Tesseract and Pytesseract.

## Architecture
### Packages
- [**pillow**](https://python-pillow.org/): a Python package for manipulating images
- [**pytesseract**](https://github.com/madmaze/pytesseract): Python bindings for Tesseract
- [**tesseract**](https://github.com/tesseract-ocr/tesseract): a command-line program and OCR engine

### Python Standard Library
- [**os**](https://docs.python.org/3/library/os.html)

## Getting Started
### Linux & Mac OS
- This class requires an additional piece of software that is not available through PyPI. Install [tesseract](https://github.com/tesseract-ocr/tesseract) on your machine with `sudo apt-get install tesseract-ocr`
- Install Cropyble with either `pip3 install cropyble` or preferably with `pipenv install cropyble`
- Place the following import statement at the top of your file: `from cropyble import Cropyble`
- Create Cropyble instances and get to cropping!

## API
- **Cropyble()**: Takes in a string representing the input image location. Cropyble runs OCR on the image and stores the bounding boxes for recognized words and characters for future crops.
- **.crop()**: Takes in a string representing the word or character you'd like cropped from the image and a second string representing the output image path. Generates a cropped copy of the query text from the original image and saves it at the specified location.

## Change Log
07/22/2019 - 0.1.0
- Corrected bounding box math. Images are being properly cropped.

07/27/2019 - 0.2.0
- Refactored cropping functions into a class to minimize work needed to perform multiple crops on a single image.

07/30/2019 - 0.3.0
- Cropyble can now accept a path for the input image and crop() accepts a path for the output image.

08/02/2019 - 1.1.0
- Cropyble can now crop words and characters recognized within an image using the same crop() method.

10/08/19 - 1.1.4
- Refactored for packaging
- Uploaded to PyPI, bumpy ride
