# Daily Mean Temperature for Sao Paulo (2015-19)

This dataset was generated using a Random Forest model as described in the study entitled **"A satellite-based machine learning approach to estimate high resolution daily air temperature in São Paulo, Brazil"**. We developed a generalizable tree-based machine learning approach (Random Forest) to estimate daily mean temperatures at 500 x 500 metres resolution for São Paulo, Brazil. 

## Methods:
We trained a Random Forest model using open-access remote sensing data, along with derived products, and temperature measurements from 43 ground stations. To prevent overfitting and select relevant features, we employed a forward feature selection algorithm with target-oriented (spatial) cross-validation. Hyperparameter tuning was performed using grid search approach. The model was validated through ten-fold spatial cross-validation and an external hold-out dataset. The model demonstrated strong performance (RMSERF = 0.80; R²RF = 0.95), with slightly reduced accuracy in rural areas (R²rural = 0.91; R²urban = 0.95). Compared to traditional multilinear approaches (RMSEMLR = 1.02; R²MLR = 0.92), the Random Forest model outperformed, likely due to its ability to better capture microclimates and complex relationships between data sources. 

## Why is it important?
Spatiotemporally resolved ambient temperature data is essential for environmental epidemiological studies, particularly in densely populated and urbanized areas where temperature can vary significantly over short distances. Spatially continuous temporal records at high spatial resolution are, however, often lacking, especially in low- and middle-income countries. This 500 x 500 metres daily temperature dataset is the first of its kind in South America, with the São Paulo pipeline and data freely accessible. The approach is adaptable to other regions with appropriate retraining and validation, enabling high-resolution exposure assessments

## Metadata: 

| Parameter  | Description |
| ------------- | ------------- |
| Temporal Resolution  | Daily, Monthly, Seasonally, Annually, All period  |
| Temporal Coverage  |  2015-2019  |
| Spatial Resolution |  500m x 500m  |
| Spatial Coverage  | São Paulo municipality - bounding box  (lonmin: -46.9559; latmin: -24.0854; lonmax: -46.2226; latmax: -23.2839, coordinate reference system: WGS84)  |
| Format  | TIFF  |
| Date uploaded | 12.07.2025  |


## How to use this repository:
1. Open the 'RFTemp_PipelineApril2023.ipynb' file in Google Collab. Read the instructions.
2. Download the 'modelinput_2015_2019.zip". Extract the contents. 
3. Downlad the contents of the folder 'newdata'
4. Store the files downloaded in step 2 and 3 in the right folders, as indicated in section 1.2 of 'RFTemp_PipelineApril2023.ipynb'
5. Run the code

NOTE: This is just a test code. Does not include the full extent of the dataset. For access to all dataset, please contact the author: ainaroca16@gmail.com
