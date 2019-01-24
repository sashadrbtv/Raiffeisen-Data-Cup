# Raiffeisen Data Cup

Raiffeisenbank customers purchase and withdraw cash at ATMs with the help of cards. 
Championship participants must predict two pairs of coordinates: home coordinates (lat/lon) and work coordinates (lat/lon). 
**Evaluation** of the quality of the solution is a percentage of cases in the radius of 0.02 degrees relative to the real coordinates of the house and work.

The result of the solution is 36/547 place.

This solution includes a set of ipython notebooks to roughly illustrate the modeling process (incl. data preprocessing steps). 

*The code is quite dirty (Sorry for that)*

1) ***01_preliminary_analysis*** (short introductory analysis)

2) ***02_full_address*** (return detailed address for lat/lon data via geopy (reverse geocoding library))

3) ***03_data_preprocessing_with_some_clustering_approaches*** (some Data Preprocessing techniques, K-means and DBSCAN)

4) Modeling
    
    1) ***04_home_xgb_biclass*** (predicting home coordinates by using XGB classification model: the mean of 3 closest transactions)  
    2) ***04_home_xgb_regression*** (predicting home coordinates by using XGB classification model: the distance from transaction point to home)
    3) ***04_work_xgb_biclass*** (predicting work coordinates by using XGB classification model: the mean of 3 closest transactions)
    4) ***04_work_xgb_regression*** (predicting work coordinates by using XGB classification model: the distance from transaction point to work)

5) ***05_consolidated_results*** (mixing up the results of 4 models, some visualisation analysis with Folium)


***2018_04_05_Raiffeisen-Data-Cup.pdf*** is a presentation from a final event at Raiffeisen office (Moscow). The presentation consists of overall modeling process structure and business ideas of how to use this type of data and model results
