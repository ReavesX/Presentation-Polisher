# Presentation Polisher

**An embedded device that helps users eliminate filler words like "um" and "uh" to improve presentation fluency and boost confidence.**

Presentation Polisher is an embedded speech fluency training tool that detects and counts disfluencies in real-time. It utilizes analog signal processing and machine learning to provide immediate feedback, helping users improve their public speaking skills.

---

## Key Features

- **Real-time Speech Detection**: Uses embedded signal processing to filter and analyze speech signals in real-time.
- **Filler Word Detection**: Identifies common filler words such as "um" and "uh" and provides feedback to help users reduce their usage.
- **Machine Learning Inference**: Deploys a lightweight machine learning model for accurate and fast disfluency detection.
- **Standalone Operatfion**: The device is entirely sel-contained, using a PIC microcontroller for all processing.
- **User-Friendly Interface**: Provides visual feedback to the user, making it easy to track progress and improvements.

---

## Project Overview

The Presentation Polisher is designed to aid anyone who wants to improve their speech fluency, particularly in public speaking contexts. Whether you're a student, educator, or professional speaker, this device helps you identify and eliminate those unwanted "ums" and "uhs" from your speech, making your presentations more impactful and confident.

### **Technologies Used**
- **Embedded System**: PIC microcontrollers (e.g., PIC16F877A)
- **Signal Processing**: Analog signal processing for speech feature extraction
- **Machine Learning**: Lightweight ML models deployed for filler word detection
- **Programming Languages**: C for embedded systems, Python for ML model training

---
## Insert VIDEO HERE OF WORKING PRODUCT 
---

## Design
### Hardware
The device is built around a PIC microcontroller, with the following key features:
- **Analog Signal Processing**: Filters and processes speech signals in real-time.
- **Speech Detection**: Utilizes a microphone array for input and processes the sound for disfluency detection.

Refer to the [hardware design documentation](docs/hardware_design.md) for details on circuit schematics and PCB layout.
---
### Software
The software is modular, focusing on the following areas:
- **Speech Signal Processing**: Filters raw audio input and extracts features relevant to filler word detection.
- **Disfluency Detection**: Uses machine learning models trained to recognize "um" and "uh".
- **Feedback System**: Displays real-time feedback to the user, guiding them in reducing filler words.

Check the [software design documentation](docs/software_design.md) for an in-depth explanation of the architecture and flow.

<details>
<summary>File Structure Overview</summary>
<br>
        /Presentation-Polisher
        │
        ├── /docs                          # Documentation related to the project
        │   ├── project_overview.md         # High-level project description and goals
        │   ├── hardware_design.md          # Schematic diagrams, PCB designs
        │   ├── software_design.md          # Detailed software architecture
        │   ├── machine_learning.md         # ML model training and deployment
        │   └── troubleshooting.md          # Debugging tips, issues, and solutions
        │
        ├── /hardware                       # Hardware-related files
        │   ├── /schematics                 # Circuit diagrams, electrical schematics
        │   ├── /PCB_design                 # PCB layout files
        │   └── /components                 # Lists of components, datasheets, and BOM
        │
        ├── /software                       # Source code for the embedded system
        │   ├── /src                        # Main source files
        │   │   ├── main.c                  # Main program entry point
        │   │   ├── filler_counter.c           # Logic to detect "um" and "uh" and process speech
        │   │   ├── signal_processing.c     # Analog signal processing functions
        │   │   └── ml_inference.c          # Machine learning model inference and predictions
        │   │
        │   ├── /include                    # Header files
        │   │   ├── filler_counter.h           # Function declarations for disfluency detection
        │   │   ├── signal_processing.h     # Header for signal processing
        │   │   └── ml_inference.h          # Header for ML-related functions
        │   │
        │   ├── /lib                        # External libraries (e.g., ML library, signal processing)
        │   │   └── ml_model                # Pretrained model files (e.g., .h or .bin)
        │   │
        │   └── /build                      # Build folder (generated during compilation)
        │       ├── /debug                  # Debug build output
        │       └── /release                # Release build output
        │
        ├── /test                           # Unit tests and mock hardware test scripts
        │   ├── /unit_tests                 # Unit tests for the functions
        │   ├── /mock_hardware              # Mock hardware simulations for testing
        │   └── /test_report.md             # Test cases, results, and analysis
        │
        ├── /scripts                        # Useful scripts for project automation
        │   ├── build.sh                    # Build script (e.g., for setting up the toolchain)
        │   ├── flash_device.sh              # Script to flash the PIC microcontroller
        │   └── train_model.py               # Python script for training the ML model
        │
        ├── /config                         # Configuration files
        │   ├── /pin_mapping.h              # Pinout and hardware configuration settings
        │   ├── /device_config.h            # Microcontroller-specific settings
        │   └── /ml_config.h                # Configuration for the machine learning model
        │
        ├── /docs/model_training            # Specific directory for model training files
        │   ├── training_data.csv           # Raw training data (audio features)
        │   ├── model_code.py               # Python code to preprocess data and train models
        │   ├── trained_model.h             # Exported model in embedded format
        │   └── evaluation_results.md       # Metrics and evaluation of trained model
        │
        └── README.md                       # Overview of the project, installation steps, etc.
</details>
## Getting Started

## Getting started:
To get started with the Presentation Polisher, you’ll need the following:

### **Prerequisites**
- PIC microcontroller programmer (e.g., PICkit 3 or PICkit 5)
- Microcontroller development environment (e.g., MPLAB X IDE, XC8 compiler)
- Python (for model training and evaluation)

### **Installation**

1.) Clone the repository:
   
   bash
   ```git clone https://github.com/yourusername/Presentation-Polisher.git```
2.) Build the project:
    2a) Navigate to the /software directory.
    2b) Use MPLAB X IDE or your preferred development environment to build the project and flash it onto your PIC microcontroller.
3.) Train the machine learning model:
    3a) Use the provided Python script (train_model.py) to train your model. The script takes audio feature data as input and outputs a trained model that can be used for disfluency detection.
        bash
        ```python train_model.py ```
4.) Flash the device with the new firmware and start using the device for real-time disfluency detection!

## License
This project is licensed under the MIT License - see the LICENSE file for details.
