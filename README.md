# YOLO RB3Gen2 Trainer

Instruction set for running powerful and efficient YOLOv8-based object detection training pipeline on **RB3Gen2**, optimized for custom dataset training with advanced configuration options. 

## 🚀 Features

- Yolov8 Setup for RB3Gen2
  - Quantization and Compiliation
- YOLOv8 model support with multiple architecture options (nano to extra-large)
- Configurable training parameters through YAML configuration
- Support for both CPU and CUDA training
- Advanced training optimizations including:
  - Cosine learning rate scheduling
  - Mixed precision training
  - Rectangular training for memory efficiency
  - Mosaic augmentation
  - Label smoothing
  - Dropout regularization


## 📋 Prerequisites

- Google Account
- RB3Gen2

## 🛠️ Installation

1. Open .ipynb and click the link "Open in Collab"
2. Make sure you're using a T4 GPU Runtime

## ⚙️ Configuration

The project uses a `config.yaml` file for all training parameters. Key configuration sections include:

- Model Configuration: Choose YOLOv8 model size and pretrained options
- Dataset Configuration: Set training/validation data paths and number of classes
- Training Configuration: Fine-tune training parameters like epochs, batch size, etc.

Example configuration:
```yaml
model:
  type: 'yolov8n'  # Options: yolov8n, yolov8s, yolov8m, yolov8l, yolov8x
  pretrained: true

data:
  train: 'data/train'
  val: 'data/val'
  nc: 1  # Number of classes
```

## 📁 Project Structure

```
yolo-rb3gen2-trainer/
├── config.yaml           # Training configuration
├── requirements.txt      # Project dependencies
├── training_images/      # Training dataset directory
└── base_image.jpg       # Base image for reference
```

## 🎯 Usage

1. Prepare your dataset in the `training_images` directory
2. Update the `config.yaml` file with your specific requirements
3. Open the ipynb in collab and run it then follow the instructions in the Jupyter Notebook

## 📊 Training Parameters

The training pipeline supports various parameters for YOLOv8 that can be configured in `config.yaml`:

- `epochs`: Number of training epochs
- `batch_size`: Batch size for training
- `imgsz`: Input image size
- `device`: Training device (cuda/cpu)
- `optimizer`: Choice of optimizer (SGD/Adam)
- And many more advanced options

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Ultralytics YOLOv8
- PyTorch
- OpenCV
- And all other open-source libraries used in this project
