<div align="center">
<h1>
   <img src="https://img.icons8.com/pulsar-color/96/markdown.png" width="100" height="100" />
   <br>
   FDT5_MODEL
</h1>
<h3>◦ FDT5_Model: Transforming AI with Simplicity and Power</h3>
<h3>◦ Developed with the software and tools below.</h3>

<p align="center">
<img src="https://img.shields.io/badge/tqdm-FFC107.svg?style=flat&logo=tqdm&logoColor=black" alt="tqdm">
<img src="https://img.shields.io/badge/SciPy-8CAAE6.svg?style=flat&logo=SciPy&logoColor=white" alt="SciPy">
<img src="https://img.shields.io/badge/Python-3776AB.svg?style=flat&logo=Python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/GitHub-181717.svg?style=flat&logo=GitHub&logoColor=white" alt="GitHub">

<img src="https://img.shields.io/badge/pandas-150458.svg?style=flat&logo=pandas&logoColor=white" alt="pandas">
<img src="https://img.shields.io/badge/NumPy-013243.svg?style=flat&logo=NumPy&logoColor=white" alt="NumPy">
<img src="https://img.shields.io/badge/JSON-000000.svg?style=flat&logo=JSON&logoColor=white" alt="JSON">
<img src="https://img.shields.io/badge/Markdown-000000.svg?style=flat&logo=Markdown&logoColor=white" alt="Markdown">
</p>

![license](https://img.shields.io/github/license/kennysuper007/FDT5_Model?style=flat&labelColor=E5E4E2&color=869BB3)
![repo-language-count](https://img.shields.io/github/languages/count/kennysuper007/FDT5_Model?style=flat&labelColor=E5E4E2&color=869BB3)
![repo-top-language](https://img.shields.io/github/languages/top/kennysuper007/FDT5_Model?style=flat&labelColor=E5E4E2&color=869BB3)
![last-commit](https://img.shields.io/github/last-commit/kennysuper007/FDT5_Model?style=flat&labelColor=E5E4E2&color=869BB3)
</div>

---

## 🔗 Quick Links
- [🔗 Quick Links](#-quick-links)
- [📍 Overview](#-overview)
- [📂 Repository Structure](#-repository-structure)
- [🧩 Modules](#-modules)
- [🚀 Getting Started](#-getting-started)
  - [⚙️ Installation](#️-installation)
  - [🤖 Running FDT5\_Model](#-running-fdt5_model)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [👏 Acknowledgments](#-acknowledgments)

---

## 📍 Overview
The FDT5_Model is a system capable of generating engaging questions from specified locations, represented by a vehicle's GPS coordinates and four side street-view images captured by on-car cameras. We utilize data from the Google Street View dataset and craft prompts based on the address obtained through reverse geocoding of the GPS coordinates, complemented by captions from street-view images generated by an advanced image captioning model. This repository demonstrates the use of street views and coordinates from various locations including USA_Pittsburgh, USA_Orlando, USA_NewYork, and Taiwan_Kaohsiung, to create engaging questions.

---

## 📂 Repository Structure

```sh
└── FDT5_Model/
    ├── StreetviewFilter/
    │   └── checkpoint-27100/
    │       └── config.json
    ├── checkpoints/
    │   └── DistilledStreetviewFilter_T5LargeTeacher/
    │       └── checkpoint-54000/
    ├── count_vocab.py
    ├── dataset.py
    ├── model.py
    ├── requirements.txt
    ├── results/
    │   ├── Taiwan_Kaohsiung.json
    │   ├── USA_NewYork.json
    │   ├── USA_Orlando.json
    │   └── USA_Pittsburgh.json
    ├── single_inference.py
    ├── streetview_images/
    │   ├── Taiwan_Kaohsiung/
    │   ├── USA_NewYork/
    │   ├── USA_Orlando/
    │   └── USA_Pittsburgh/
    ├── utils_classifier.py
    └── 指令.txt

```

---

## 🧩 Modules

<details closed><summary>.</summary>

| File                                                                                             | Summary                                                                                                                                                                                                                                                                                                                                                                                                   |
| ---                                                                                              | ---                                                                                                                                                                                                                                                                                                                                                                                                       |
| [requirements.txt](https://github.com/kennysuper007/FDT5_Model/blob/main/requirements.txt)       | The code snippet in the `FDT5_Model` repository is responsible for filtering and processing street view images. It utilizes dependencies such as `transformers` and `torch` to achieve this. The main files involved are `count_vocab.py`, `dataset.py`, `model.py`, and `single_inference.py`. The codebase also includes directories for checkpoints, results, street view images, and utility scripts. |
| [count_vocab.py](https://github.com/kennysuper007/FDT5_Model/blob/main/count_vocab.py)           | This code snippet is responsible for building a vocabulary based on a given text file. It counts the frequency of words in the text and discards words below a specified threshold. The resulting vocabulary is stored with word-to-index and index-to-word mappings. The main file takes command-line arguments for the text file path and threshold value.                                              |
| [指令.txt](https://github.com/kennysuper007/FDT5_Model/blob/main/指令.txt)                           | The code snippet in the `single_inference.py` file performs single inference on street view images using given coordinates and locations. It is part of the FDT5_Model repository and relies on dependencies listed in `requirements.txt`.                                                                                                                                                                |
| [model.py](https://github.com/kennysuper007/FDT5_Model/blob/main/model.py)                       | This code snippet is part of the FDT5_Model repository and contributes to its architecture. It includes dependencies such as torch and transformers, and defines key files like model.py. The code implements T5-based model operations, including self-attention, cross-attention, and feed-forward layers.                                                                                              |
| [dataset.py](https://github.com/kennysuper007/FDT5_Model/blob/main/dataset.py)                   | This code snippet is part of a larger codebase with a specific directory structure. It depends on the dataset.py file and uses various imports. The main file in this snippet is responsible for initializing a Dataset object, setting various parameters, and preprocessing data if the CLIP library is used.                                                                                           |
| [utils_classifier.py](https://github.com/kennysuper007/FDT5_Model/blob/main/utils_classifier.py) | The code snippet contains a Python class called EngagingDataset, which is responsible for creating and managing a dataset for training a machine learning model. It includes methods for preprocessing and organizing the data, as well as for batching and retrieving predictions. The class utilizes dependencies such as torch, pandas, and DataLoader.                                                |
| [single_inference.py](https://github.com/kennysuper007/FDT5_Model/blob/main/single_inference.py) | The code snippet in `single_inference.py` is a key file in the repository architecture. It uses various dependencies and software tools to perform single inference tasks for streetview images. It utilizes transformers, torch, pandas, and googlemaps to process data and generate results.                                                                                                            |

</details>

<details closed><summary>StreetviewFilter.checkpoint-27100</summary>

| File                                                                                                               | Summary                                                                                                                                                                                                                                                    |
| ---                                                                                                                | ---                                                                                                                                                                                                                                                        |
| [config.json](https://github.com/kennysuper007/FDT5_Model/blob/main/StreetviewFilter/checkpoint-27100/config.json) | The code snippet in the StreetviewFilter directory implements a T5 model for conditional generation. It uses a pre-trained T5 model to generate questions based on given input. The model architecture and parameters are defined in the config.json file. |

</details>

<details closed><summary>checkpoints.DistilledStreetviewFilter_T5LargeTeacher.checkpoint-54000</summary>

| File                                                                                                                                                   | Summary                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---                                                                                                                                                    | ---                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [config.json](https://github.com/kennysuper007/FDT5_Model/blob/main/checkpoints/DistilledStreetviewFilter_T5LargeTeacher/checkpoint-54000/config.json) | This code snippet is part of the FDT5_Model repository. It includes key files such as `model.py`, `dataset.py`, and `single_inference.py`. The main role of this code is to provide functionality for training and using a T5-based model for conditional generation. It makes use of dependencies such as the Transformers library and a pre-trained checkpoint for the model. The code allows for dataset processing, model training, and inference to generate text based on input data. |

</details>

<details closed><summary>results</summary>

| File                                                                                                         | Summary                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ---                                                                                                          | ---                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [USA_Pittsburgh.json](https://github.com/kennysuper007/FDT5_Model/blob/main/results/USA_Pittsburgh.json)     | This code snippet is part of the FDT5_Model repository. It contributes to the architecture by providing functionalities for street view filtering and classification. It includes key files such as dataset.py, model.py, and utils_classifier.py. The codebase has dependencies and uses software like TensorFlow. The repository layout consists of directories for street view images, checkpoints, and results. The results directory contains JSON files for different cities like USA_Pittsburgh.json.                                                                                                                                                                                                                       |
| [USA_Orlando.json](https://github.com/kennysuper007/FDT5_Model/blob/main/results/USA_Orlando.json)           | The code snippet in the `FDT5_Model` repository is responsible for analyzing streetview images and generating prompts for users to engage in conversation about the images. The code achieves this by using a model to generate questions based on the images, allowing users to discuss various aspects such as architectural features, landmarks, local businesses, and traffic flow. The codebase includes key files such as `model.py`, `dataset.py`, and `single_inference.py`, which are used for model training, data preparation, and inference, respectively. The repository also contains relevant directories for checkpoints, streetview images, and result files.                                                     |
| [Taiwan_Kaohsiung.json](https://github.com/kennysuper007/FDT5_Model/blob/main/results/Taiwan_Kaohsiung.json) | This code snippet is part of the FDT5_Model repository and is responsible for generating captions for street view images. It utilizes a model and dataset to provide summaries of key aspects of the images, such as cleanliness, architecture, landmarks, and businesses in the area.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [USA_NewYork.json](https://github.com/kennysuper007/FDT5_Model/blob/main/results/USA_NewYork.json)           | The code snippet in the single_inference.py file of the FDT5_Model repository is responsible for generating questions about street views in different cities. It uses a pre-trained model to generate various questions about the streets and landmarks observed in the images. The code processes the street view images, extracts features, and utilizes natural language processing techniques to generate descriptive and thought-provoking questions. The generated questions can be about the architecture, businesses, landmarks, traffic, and other aspects of the streets in various cities. The code enables users to gain insights into the characteristics of different streets and engage in interactive discussions. |

</details>

---

## 🚀 Getting Started

### ⚙️ Installation

1. Clone the FDT5_Model repository:
```sh
git clone https://github.com/kennysuper007/FDT5_Model
```

2. Change to the project directory:
```sh
cd FDT5_Model
```

### 🤖 Running FDT5_Model
Use the following command to run FDT5_Model:
```sh
python3 single_inference.py --coordinate 22.6408282,120.3222442 --location Taiwan_Kaohsiung
python3 single_inference.py --coordinate 40.440309,-80.0 --location USA_Pittsburgh
python3 single_inference.py --coordinate 28.541323,-81.380703 --location USA_Orlando
python3 single_inference.py --coordinate 40.73055,-74.001715 --location USA_NewYork
```

---

## 🤝 Contributing

Contributions are welcome! Here are several ways you can contribute:

- **[Submit Pull Requests](https://github.com/kennysuper007/FDT5_Model/blob/main/CONTRIBUTING.md)**: Review open PRs, and submit your own PRs.
- **[Join the Discussions](https://github.com/kennysuper007/FDT5_Model/discussions)**: Share your insights, provide feedback, or ask questions.
- **[Report Issues](https://github.com/kennysuper007/FDT5_Model/issues)**: Submit bugs found or log feature requests for FDT5_Model.

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your GitHub account.
2. **Clone Locally**: Clone the forked repository to your local machine using a Git client.
   ```sh
   git clone <your-forked-repo-url>
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear and concise message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to GitHub**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.

Once your PR is reviewed and approved, it will be merged into the main branch.

</details>

---

## 📄 License


This project is protected under the MIT License. For more details, refer to the [LICENSE](https://choosealicense.com/licenses/) file.

---

## 👏 Acknowledgments

- I modified the inference commands to demonstrate the capabilities of the FDT5 model trained by Nicholas.

---
