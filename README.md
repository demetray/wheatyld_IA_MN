# wheatyld_IA_MN
SML310 Final Project: comparison of 6 different regression models for predicting wheat yield in Iowa and Minnesota
The files in this repository are used to develop a wheat yield model for Minnesota and Iowa based on meteorological parameters from the ERA5 dataset. Annual wheat yield data is taken from gro-intelligence. 


# PRE-PROCESSING ANNUAL WHEAT YIELD DATA

wheat_bydistrict: gro-intelligence annual wheat yield data by district, contiguous US (Sheet 1), lat/lon coordinates for counties in MN and IA (Sheet 6 and 7), yields in MN and IA (sheet 3). 

ylds_ia_mn.ipynb: read in lat/lon coordinates for counties in MN and IA, and store lat/lon columns in wheat yields dataframe

wheatf_mn_ia.xlsx: wheat yields in IA and MN with corresponding lat/lon coords stored in columns



# PRE-PROCESSING ERA5 DATA

*Note: all files beginning with “extract” require ERA5 data files in format, netCDF4. I accessed these through Princeton University’s tigress database on the tiger cpu. These files are very large, so I deleted each one after extraction to make space for the other data. So, I have not redownloaded them to upload them here. 

extract_mean_precip.ipynb: extract monthly mean total precipitation rate at year/lat/lon of wheat yield data for each month

extract_rh.ipynb: extract monthly mean relative humidity at year/lat/lon of wheat yield data for each month

extract_mean_precip.ipynb: extract monthly mean total precipitation rate at year/lat/lon of wheat yield data for each month

extract_t2m_avg_monthly.ipynb: extract monthly mean temperature at 2m at year/lat/lon of wheat yield data for each month

extract_t2m_extr.ipynb: extract monthly max and min t2m at year/lat/lon of wheat yield data for each month

extract_uv.ipynb: extract monthly mean surface downward uv radiation at year/lat/lon of wheat yield data for each month

get_anomalies.ipynb: get anomalies based on monthly expected value at lat/lon of all features extracted from files above



# ALL FEATURES PRE-PROCESSED DATA

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



# EXPLORATORY DATA ANALYSIS

eda.ipynb: plots of yield vs each feature



# NARROWED DOWN FEATURES FOR MODEL INPUT

finalfeat.xlsx
finalfeat_index.xlsx



# MODEL

yld_model.ipynb: script for comparison of 6 different regressions for predicting wheat yield


