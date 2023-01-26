# LitBryo: Mining the literature for specimen images 

## Description

This repository contains code for mining images of bryozoan specimens from PDF files using the pdffigures2.0 library developed by AllenAI. The approach used in this repository is as follows:

- Extraction of images and captions from PDF files using pdffigures2.0
- Cleaning of non-relevant figures by embedding them using a pretrained vision model
- Clustering of images based on their embeddings
- Selection of the cluster containing the specimen images

## Dependencies
This repository requires the following dependencies to be installed:

- pdffigures2.0 (https://github.com/allenai/pdffigures2)
- A pretrained vision model (e.g. ResNet, VGG, etc.)
- Python 3.7

## Usage

To run on lots of PDFs while saving the images, figure objects, and run statistics:
```
sbt "runMain org.allenai.pdffigures2.FigureExtractorBatchCli /path/to/pdf_directory/ -s stat_file.json -m /figure/image/output/prefix -d /figure/data/output/prefix"
```
To perform image embeddings using pretrained models:
- Select your model of choice 
- Use the approach described within `image_embeddings.ipynb`

A `csv` file contaning the image paths that contain bryozoan SEMs will be produced.


