# tsunami_eo_analysis

# Steps to run code

1. Clone repository to local device.
2. Create conda evironment.
3. pip install -r requirements.txt
4. Create the following folders in a folder named "data":
  - pre_tsunami
  - eight_days_post_tsunami
  - one_month_post_tsunami
    
  with satellite data including separate bands. If renamed, adjust analysis input in notebook.
  To recreate analysis previously done, these folders can be filled with the relevant Landsat 5 data IDs collected from https://earthexplorer.usgs.gov:
  - pre_tsunami: LS5 ID = LT05_L2SP_142053_20040202_20200904_02_T1_
  - eight_days_post_tsunami: LS5 ID = LT05_L2SP_142053_20050103_20200902_02_T1_
  - one_month_post_tsunami: LS5 ID = LT05_L2SP_142053_20050204_20200902_02_T1_
5. Store .geojson containing area in question in the same data folder.
6. Adjust analysis inputs to suit analysis, including:
  - files_for_analysis = list of files in question, maximum of 3. Must match folder names.
  - geojson_area_of_interest = location of cropping vector polygon file.
  - bands_of_interest = list of band numbers used for initial analysis, must be in numerical order and not skipping any values.
  - bands_for_classification = similar to above, list of band numbers used for classification, default set to all available bands.
  - band_dict = specifies band information for specific satellite data used, i.e. Landsat 5.
7. To use the CNN_tool, the TerraFM-B.pth needs to be downloaded from https://huggingface.co/MBZUAI/TerraFM/tree/main to enable running of pretrained model. 
