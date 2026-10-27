# MMAD-Sentry: Multimodal System Log Anomaly Detection

This project contains Jupyter notebooks for experimenting with anomaly detection on system logs. The main notebook explores multimodal log, metric, and trace features, including cross-modal fusion, retrieval augmentation, and evaluation experiments.

## Notebooks

- **`mmad-pbl (4).ipynb`** - Main notebook with log parsing, feature preparation, and experiments for HDFS, BGL, and OpenStack.
- **`openstack-fixed (1).ipynb`** - Focused OpenStack experiment using the adjusted settings described in the notebook.

## Requirements

The notebooks install most Python dependencies in their setup cells. They expect a Python 3 Jupyter environment. The setup targets Kaggle with CUDA 12 and a GPU for PyTorch and FAISS; availability and compatibility of GPU packages depend on the environment. The notebooks do not include the datasets.

## Datasets

Place the datasets at the paths expected by the dataset-loading cells. The main notebook documents these expected files:

- `Dataset/HDFS/` - HDFS logs and preprocessed labels, event occurrence matrix, traces, templates, and feature data.
- `Dataset/BGL/` - BGL log file with labels in the log.
- `Dataset/OpenStack/` - OpenStack normal and abnormal logs and anomaly labels.

Some notebook cells use Kaggle input paths. Update those paths if running outside Kaggle.

## Running

1. Open a notebook in Jupyter or Kaggle.
2. Make the required datasets available and confirm the paths in the dataset-loading cells.
3. Run the setup and preparation cells from top to bottom.
4. Run the experiment cells you want. For the OpenStack fixed experiment, use `openstack-fixed (1).ipynb`.

The experiments may require substantial memory and compute, particularly when using transformer models and GPU-based FAISS.
