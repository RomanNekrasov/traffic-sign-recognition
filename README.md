# Traffic Sign Recognition

## About the Project
Welcome to the GitHub Repository of our project for the Deep Learning course at JADS. We trained a traffic sign 
classifier using synthetic data and tested it on real-world images from scanning cars. Our best performing model
achieved an accuracy of 82.4%.

### MLOps Setup
Initially, we faced challenges setting up a suitable environment for machine learning practices on Google Cloud 
Platform (GCP) because the GCP credits provided did not allow us to create Virtual Machines (VMs) with Graphical 
Processing Units (GPUs). We then discovered Vertex AI, where we successfully set up our automated training pipeline 
using multiple Tesla T4 GPUs. The models were created using PyTorch, and we saved the model metrics and the best 
performing models to cloud storage using TensorBoard.


### Build With
[![Python 3.11](https://img.shields.io/badge/Python-3.11-3776AB)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.2.2-EE4C2C)](https://pytorch.org/)
[![Google Cloud Vertex AI](https://img.shields.io/badge/Google%20Cloud-Vertex%20AI-4285F4)](https://cloud.google.com/vertex-ai)

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/your_username/traffic-sign-recognition.git
    ```
2. Navigate to the project directory:
    ```sh
    cd traffic-sign-recognition
    ```
3. Create a virtual environment:
    ```sh
    python -m venv venv
    ```
4. Activate the virtual environment:
    - On Windows:
        ```sh
        venv\Scripts\activate
        ```
    - On macOS and Linux:
        ```sh
        source venv/bin/activate
        ```
5. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

## Repository setup

### 1. **Structure**

```plaintext
.
├── 1_dino_pipeline.ipynb
├── 2_data_pipeline.ipynb
├── 3_train_pipeline.ipynb
├── 4_evaluate.ipynb
├── 5_benchmark_notebook.ipynb
├── README.md
├── data
│   ├── test_data
│   └── train_templates
├── metrics
│   ├── augmentations
│   ├── batch_experiment
│   ├── dropout_experiment
│   ├── l2
│   └── plots
├── Nekrasov, Huang & Van de Voort (2024).pdf
├── correct_classified_images.pdf
├── misclassified_images.pdf
└── requirements.txt
```


### 2. **File and Directory Descriptions**

```markdown
| File/Directory                            | Description                                                                           |
|-------------------------------------------|---------------------------------------------------------------------------------------|
| `1_dino_pipeline.ipynb`                   | Code for object detection of the raw data with Grounding DINO                         |
| `2_data_pipeline.ipynb`                   | Data augmentation notebook.                                                           |
| `3_train_pipeline.ipynb`                  | Training pipeline for the model, including setup for hyperparameters.                 |
| `4_evaluate.ipynb`                        | Evaluation to assess model performance on test data.                                  |
| `5_benchmark_notebook.ipynb`              | Test results benchmarked against DenseNet169.                                         |
| `Nekrasov, Huang & Van deVoort (2024).pdf`| The final report of our work.                                                         |
| `correct_classified_images.pdf`           | a PDF report of correctly classified images by the best version of the model.         |
| `misclassified_images.pdf`                | a PDF report of misclassified images by the best version of the model.                |
| `data/train_templates`                    | Contains the templates used for creating augmentations.                               |
| `data/test_data`                          | Contains labelled directories with the cropped real world signs.                      |
| `metrics/`                                | The metrics for each experimental setup, as discussed in the paper                    |
| `metrics/plots`                           | Plots as used in the report                                                           |
```


## Authors
- [Andy Huang](https://github.com/andyhuangNL)
- [Huub van de Voort](https://github.com/hvdv99/)
- [Roman Nekrasov](https://github.com/RomanNekrasov/)

## Additional Resources
- [JADS Course Description](https://uvt.osiris-student.nl/onderwijscatalogus/extern/examenprogramma/36700/3N300-2022?taal=en)