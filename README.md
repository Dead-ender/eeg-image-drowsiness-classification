# EEG-Derived Image Classification for Drowsiness Experiments

A TensorFlow/Keras notebook that standardizes EEG-like arrays, converts signals into images, and trains an image classifier for awake/drowsy labels. Despite the original filename, the notebook does not implement facial landmarks, eye-aspect-ratio calculations, or real-time camera inference.

## Data and limitations

The source arrays DrowD.npy and label.npy are not included. The notebook expects them under data/ and writes intermediate images/features under data/. It also contains a fixed-size reshape tied to the original dataset; update it for different sample counts. Outputs were removed, and no validated performance claim is made.

No datasets, checkpoints, or model weights are included. Notebook outputs were cleared to remove stale runtime logs and generated figures. The training and evaluation cells remain part of the notebook but were not rerun during repository preparation; this README makes no performance or real-world accuracy claim.

## Requirements

- Python 3.10 or newer
- Dependencies listed in `requirements.txt`
- TensorFlow uses the Keras 2 API; TensorFlow 2.12–2.15 is the intended compatibility range. Install a build appropriate for your platform and hardware.

```bash
python -m venv .venv
# Activate the environment, then:
python -m pip install -r requirements.txt
```

## Run

Open `notebook.ipynb` in Jupyter or Google Colab. Review the data paths and labels before running. Several source notebooks contain exploratory or dataset-specific assumptions that may need adjustment for a different dataset.

## Tests

The tests validate notebook structure and confirm that generated execution outputs are absent. They do not execute model training or verify predictive performance.

```bash
python -m pip install pytest
python -m pytest
```
