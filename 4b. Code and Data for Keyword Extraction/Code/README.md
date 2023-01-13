# CBSA-Data-analytic-challenge-021 Documentation

## Program structure

### The program automatically generates folders.

- **analysis**  to store intermediate files generated by the analysis data.
- **data**  to store the raw data.

### The program generated files.

- **wordcloud.jpg**  Word cloud files generated for top ranking keywords.
- **sourcetime.jpg**  Line graph of the trend of the number of each comment source over time.

### The important structure.

- **map_dataset: 'dict[docid:[line]]'**  A dictionary that stores the correspondence between ids and data rows.
- **map_nkey: 'dict[docid:[n_keywords]]'**  A dictionary that stores the correspondence between ids and keywords.
- **source_key_dict: 'dict[source:set(docid)]'**  A dictionary that stores the correspondence between groups and published statements.

## User Manual

1. Download the files, first run the code once, it will create two files data and analysis, it will report an error indicating that the data file is missing.
2. First copy the new_analytics_challenge_dataset_edited.xlsx data file to the data directory, then run the program to convert the data file (3 minutes), and set the DEBUG mode to False.
3. The data conversion will take about 3 minutes and will generate a .pkl file under the data directory for fast data reading.
4. Then the program will extract the keywords of each data item for subsequent analysis. The keywords are extracted using jieba's python library (which needs to be installed in advance), and the process takes about 2 hours.
5. If you don't want to wait two hours and don't need to set additional parameters, copy analysis_nkey_array.pkl to the analysis folder.
6. Running the file directly will generate the corresponding analysis files under the analysis folder.
7. The analysis files are analysis of time, analysis of comment sentiment, and extraction of content of interest.
8. More accurate keyword extraction, and high frequency keyword.
9. Graph of keyword sources and temporal changes in the number of comments by camp.
10. Output different data information according to different keywords and save it as .csv.

## Finals

CBSA-Wizers Analytics Chanllenge: Third Place.

1. Data cleaning: Processing the data given by the final.
2. Determining key influences on the accuracy of curve fitting using polynomial regression.
3. The grid searches for ratios between multiple factors and selects the ratio with the greatest accuracy as the coefficient between predictors.

`Arrivals = -33.180 + 0.292*HongKong_infections + 4.683*Mainland_infections + 0.210*Asian_infections - 0.904*European_American_infections + 0.016*Vaccination - 0.009*policy`

## Project Experience
```
CBSA-Wiser Analytics Challenge 2022 : Look for potential links between the number of arrivals and social media talk factors and try to predict the fit to past data.
1. collaborative multi-person development using git team.
2. Python language to manipulate data files, and data cleaning, sorting and integration of data by time interval according to social media posting time.
3. using multi-process scheduling multi-threaded parallelism to speed up the analysis of the sentiment analysis module cnsenti.
4. Use polynomial regression single factor by accuracy to analyze social media factors related to the number of influential arrivals.
5. Use model fitting and grid search to predict the proportion of correlation between factors.
```

```
CBSA-Wiser Analytics Challenge 2022 : 寻找入境人数与社交媒体谈论因素之间的潜在联系，并尝试预测拟合过往数据。
1. 使用git团队多人协同开发。
2. Python语言操作数据文件，并进行数据清洗，按照社交媒体发布时间按时间间隔对数据进行排序和整合。
3. 使用多进程调度多线程并行加快情感分析模块cnsenti分析速度。
4. 使用多项式回归单因素按准确率分析影响入境人数相关的社交媒体因素。
5. 使用模型拟合和网格化搜索预测各因素之间的相关比例。
```