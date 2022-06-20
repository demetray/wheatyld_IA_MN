# wheatyld_IA_MN

SML310 Final Project: comparison of 6 different regression models for predicting wheat yield in Iowa and Minnesota

The files in this repository are used to develop a wheat yield model for Minnesota and Iowa based on meteorological parameters from the ERA5 dataset. Annual wheat yield data is taken from gro-intelligence.


# Pre-processing annual wheat yield data

wheat_bydistrict.xlsx: gro-intelligence annual wheat yield data by district, contiguous US (Sheet 1), lat/lon coordinates for counties in MN and IA (Sheet 6 and 7), yields in MN and IA (sheet 3). 

ylds_ia_mn.ipynb: read in lat/lon coordinates for counties in MN and IA, and store lat/lon columns in wheat yields dataframe



# Pre-processing ERA5 data

Note: all files beginning with “extract” require ERA5 data files in netCDF4 format. I accessed these through Princeton University’s tigress database on the tiger cpu. These files are very large, so I deleted each one after extraction to make space for the other data. So, I have not redownloaded them to upload them here. 

extract_era5

    extract_mean_precip.ipynb: extract monthly mean total precipitation rate at year/lat/lon of wheat yield data for each month

    extract_rh.ipynb: extract monthly mean relative humidity at year/lat/lon of wheat yield data for each month

    extract_mean_precip.ipynb: extract monthly mean total precipitation rate at year/lat/lon of wheat yield data for each month

    extract_t2m_avg_monthly.ipynb: extract monthly mean temperature at 2m at year/lat/lon of wheat yield data for each month

    extract_t2m_extr.ipynb: extract monthly max and min t2m at year/lat/lon of wheat yield data for each month

    extract_uv.ipynb: extract monthly mean surface downward uv radiation at year/lat/lon of wheat yield data for each month

    get_anomalies.ipynb: get anomalies based on monthly expected value at lat/lon of all features extracted from files above



# All pre-processed data

era5_preprocessed

    monthly_avg_temp.xlsx
    monthly_max_t2m.xlsx
    monthly_min_t2m.xlsx
    monthly_precip_rate.xlsx
    monthly_uv_max.xlsx
    monthly_uv_mean.xlsx
    monthly_avgt2m_anom.xlsx
    monthly_maxt2m_anom.xlsx
    monthly_mint2m_anom.xlsx
    monthly_precipr_anom.xlsx
    monthly_uvmax_anom.xlsx
    monthly_uvmean_anom.xlsx
    monthly_uv_min.xlsx
    monthly_uv_min_anom.xlsx
    monthly_rh_mean.xlsx
    monthly_rh_mean_anom.xlsx

wheatf_mn_ia.xlsx



# Exploratory data analysis

eda.ipynb: plots of yield vs each feature



# Narrowed down features for model input

The files here contain 62 features, narrowed down from the original 162, based on inspection of yield vs feature plots in the exploratory data analysis.

finalfeat.xlsx

finalfeat_index.xlsx



# Model

yld_model.ipynb: script for comparison of 6 different regressions for predicting wheat yield



# Final Report

Final_Report.pdf: report submitted for completion of SML310: Research Projects in Data Science (Princeton University, Fall 2021) course requirements

Final_Report_Appendix.pdf: appendix associated with final report

# CITATION

If you have found this software or report helpful, please cite as follows:

Yancopoulos, D. (2021). *A Comparison of Several Multivariate Linear and Polynomial Regressions for Modeling Wheat Yield in Minnesota and Iowa*. Unpublished research. Princeton University Statistics and Machine Learning Department. https://github.com/demetray/wheatyld_IA_MN

