#aianalyze

This repository contains a Colab notebook `boan_data_pipeline.ipynb` that downloads MLTMA press releases, converts them to text with layout information, and indexes the results in SQLite and FAISS.

## Colab Workflow

1. **Create an environment file** on Google Drive named `aianalyze.env` inside the `boan_data` folder with the following variables (path `/content/drive/MyDrive/boan_data/aianalyze.env`):

   ```
   SERVICE_KEY=YOUR_URL_ENCODED_SERVICE_KEY
   START_DATE=2020-01-01
   END_DATE=2025-07-08
   PAGE_SIZE=1000
   DRIVE_DIR=/content/drive/MyDrive/boan_data
   HF_HOME_DIR=/content/drive/.hf_cache
   ```
   Adjust the values as needed.

2. **Open the notebook in Colab** using this link:
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/aianalyze/blob/main/boan_data_pipeline.ipynb)

3. **Run the setup cell** (mounts Drive and installs dependencies):

   ```python
   !pip install -q -r requirements.txt
   ```
4. **Execute the remaining cells** to download and index the press releases.

