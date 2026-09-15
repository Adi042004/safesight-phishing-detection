# Dataset

This folder contains the dataset used for the SafeSight phishing website detection project.

## Dataset Structure

The dataset contains URLs along with their corresponding classification labels.

| Column | Description |
|--------|-------------|
| `URL` | Website URL used for phishing detection |
| `Label` | Classification label for the URL |

Example:

| URL | Label |
|-----|-------|
| example.com | good |
| suspicious-site.com | bad |

## Labels

- `bad` — Indicates a potentially malicious/phishing URL.
- `good` — Indicates a legitimate/safe URL.

## Dataset Source

The dataset was obtained from Kaggle and is used for educational and machine-learning purposes.

The complete dataset is not included in this repository because it exceeds GitHub's web upload limit.

To reproduce the project, download the dataset and place the CSV file in this `Dataset` folder.

## Usage

The dataset is processed by the machine-learning notebooks in this project to train and evaluate the phishing website detection model.
