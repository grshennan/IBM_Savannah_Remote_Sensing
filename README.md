# XGB Classification with PALSAR-2, Sentinel-1, and Sentinel-2 Data

Author - Glen Shennan

Charles Darwin University - Research Institude for the Environment and Livelihoods - Remote Sensing and Earth Observation Research Group

<https://www.cdu.edu.au/riel/research/research-groups/remote-sensing-earth-observation>

## Description
This repository contains the main script used to produce the XGB (eXtreme Gradient Boosting) classification model using data from PALSAR-2, Sentinel-1 (S1), and Sentinel-2 (S2). This model is the best-performing model described in our upcoming article.
The script is provided for demonstration purposes only. Due to intellectual property agreements, we cannot provide the training data.

An additional script provides the download script for Sentinel-2 data from Digital Earth Australia.

## Usage
The classification script is provided as an example and cannot be run without the training data. Please refer to the provided article for a more comprehensive description of the script and its usage.

The S2 download script requires the Python libraries
1. `pystac_client`
2. `odc-stac`
3. `odc-algo`
4. `dask`
5. `rioxarray`

## Data
Due to intellectual property agreements, we cannot provide the training data. The script uses data from the following sources:
- PALSAR-2
- Sentinel-1 monthly mosaic (S1)
- Sentinel-2 (S2)

PALSAR-2 data is JAXA's yearly mosaic for 2024 <https://www.eorc.jaxa.jp/ALOS/en/dataset/fnf_e.htm>

S1 monthly mosiac data is download from the Copernicus Dataspace Ecosystem STAC <https://documentation.dataspace.copernicus.eu/APIs/STAC.html>

S2 data is downloaded from Digital Earth Australia <https://knowledge.dea.ga.gov.au/notebooks/How_to_guides/Downloading_data_with_STAC/>

Polarimetric decomposition is performed using scripts downloaded and adapted from from <https://github.com/navv37/Dual-pol-powers>

## Model
Classification is performed with XGB (eXtreme Gradient Boosting) algorithm for classification. XGB is a powerful machine learning algorithm that is particularly effective for structured data. Hyperparemeters are tuned with sequential `RandomizedSearchCV` and `GridSearchCV` runs.

## Results
The classification script produces the best-performing classification model as described in the article. The results include the classification accuracy and other relevant metrics.

## Citation
If you use this code or data in your research, please cite our article.

```bibtex
@article{shennan2026,
  title={Title of the Article},
  author={Shennan, Glen and Younis, Sam and Legge, Sarah and Murphy, Brett and Environmental Services Unit, Nyamba Buru and Crabbe, Richard},
  journal={Journal Name},
  volume={Volume},
  number={Number},
  pages={Pages},
  year={2026},
  publisher={Publisher},
  doi={DOI}
}
