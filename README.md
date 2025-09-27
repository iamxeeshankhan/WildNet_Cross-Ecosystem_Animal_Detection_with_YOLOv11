# WildNet: Cross-Ecosystem Animal Detection with YOLOv11

A multi-domain animal detection system that combines datasets from terrestrial, aerial, and aquatic ecosystems to train a comprehensive YOLOv11 model for wildlife recognition.

## Overview

This project integrates six diverse animal datasets to create a unified detection system capable of identifying animals across different environments. The model is trained on YOLOv11 architecture and can detect hundreds of species from birds to marine life.

## Datasets Used

| Dataset | Domain | Description |
|---------|--------|-------------|
| CUB-200-2011 | Aerial | 200 bird species with bounding boxes |
| NABirds | Aerial | 555 North American bird species |
| Animals10 | Terrestrial | 10 common land animals (Italian dataset) |
| 90-Mix Animals | Mixed | 90 diverse animal species |
| Animals Detection | Mixed | Pre-annotated YOLO format dataset |
| Aquarium Dataset | Aquatic | Marine and freshwater species |

## Optional Fine-tuning Datasets

The following large-scale datasets can be used for additional fine-tuning, though they require significant computational resources:

| Dataset | Size | Description | Source |
|---------|------|-------------|---------|
| ImageNet Dataset | ~150GB | Large-scale image classification with 1000+ classes | [ImageNet](http://www.image-net.org/) |
| iNaturalist Dataset | ~200GB | Species identification with geo-location data | [iNaturalist](https://www.inaturalist.org/) |
| Snapshot Serengeti Dataset | 200-479GB | Camera trap images from Serengeti National Park | [LILA Science](https://lila.science/datasets/snapshot-serengeti) |

**Note**: These datasets are very large and require substantial computational resources. They are not suitable for local machines with limited hardware or Colab free-tier. Consider using cloud computing services with GPU instances for training with these datasets.

## Features

- Multi-domain animal detection (air, land, sea)
- Automated dataset processing and YOLO format conversion
- Cross-ecosystem species recognition


## Project Structure

```
├── WildNet_Cross-Ecosystem_Animal_Detection_with_YOLOv11.ipynb
├── README.md
└── yolo_dataset/
    ├── train/images/
    ├── train/labels/
    ├── val/images/
    ├── val/labels/
    ├── test/images/
    ├── test/labels/
    ├── dataset.yaml
    └── classes.txt
```

## Requirements

- Python 3.8+
- CUDA (recommended for training)
- 8GB+ RAM
- 20GB+ storage for datasets
