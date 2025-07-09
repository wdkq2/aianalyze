#aianalyze

This repository contains a Colab notebook `boan_data_pipeline.ipynb` that downloads MLTMA press releases, converts them to text with layout information, and indexes the results in SQLite and FAISS.

## Colab Workflow

1. **Create an environment file** on Google Drive named `aianalyze.env` with the following variables:
   ```
   SERVICE_KEY=YOUR_URL_ENCODED_SERVICE_KEY
   START_DATE=2020-01-01
   END_DATE=2025-07-08
   PAGE_SIZE=1000
   DRIVE_DIR=/content/drive/MyDrive/boan_data
   HF_HOME_DIR=/content/drive/.hf_cache
   ```
   Adjust the values as needed.

2. **Mount Drive and clone the repo**:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   %cd /content/drive/MyDrive
   !git clone https://github.com/your-username/aianalyze.git
   %cd aianalyze
   ```

3. **Install dependencies**:
   ```python
   !pip install -q -r requirements.txt
   ```

4. **Run the notebook** by opening `boan_data_pipeline.ipynb`, executing the first cell to load the `.env` file, then run the remaining cells.
