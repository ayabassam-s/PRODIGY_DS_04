# Prodigy InfoTech Data Science Internship Task 4

![image](https://github.com/user-attachments/assets/331d8c2a-9d17-4b88-aa29-abd97094bbff)

This report presents an analysis of traffic accident data, focusing on patterns related to road conditions, weather, time of day, and accident hotspots. The analysis utilizes a sample dataset representing US traffic accidents from the year 2020, sourced from Kaggle (https://www.kaggle.com/datasets/jonbown/us-2020-traffic-accidents). 

# Data Preparation

The dataset was downloaded from Kaggle as a collection of CSV files. For this analysis, the `acc_20.csv` file, containing accident records for 2020, was converted into an Excel file (`traffic_accidents_2020.xlsx`) to facilitate the requested Excel-based approach.

# Analysis of Road Relationship 

**Road Condition | Accident Count**   

On Roadway | 42840  
On Roadside | 7794  
In Parking Lane/Zone | 1726  
On Median | 1325  
Outside Trafficway | 486  
On Shoulder | 300  
Off Roadway-Location Unknown | 114  
Gore | 91  
Pedestrian Refuge Island or Traffic Island | 23  
Continuous Left - Turn Lane | 19  

![image](https://github.com/user-attachments/assets/65e7fd6a-4180-4edc-a674-e7455d8eca49)
Interpretation: The vast majority of accidents in this dataset occurred 'On Roadway', not necessarily at or related to a specific junction feature. 'On Roadside' is the next most common location.

#  Analysis of Weather Conditions
This section examines the weather conditions at the time of the accidents, using the `WEATHERNAME` column.
  
Weather Condition | Accident Count  
  
Clear | 38508  
Cloudy | 7194  
Rain | 4984  
Not Reported | 2761  
Snow | 785  
Fog, Smog, Smoke | 227  
Reported as Unknown | 130  
Severe Crosswinds | 49  
Blowing Snow | 33  
Sleet or Hail | 31  

![image](https://github.com/user-attachments/assets/ab46805f-9373-4c50-bcc2-2f9587651fd8)
Interpretation: Most accidents occurred during 'Clear' weather conditions. 'Cloudy' and 'Rain' conditions also account for a significant number of accidents. This suggests that while adverse weather contributes to accidents, a large number happen even in seemingly ideal conditions.


#  Analysis of Time of Day Patterns

This section analyzes accident frequency based on the hour of the day and the day of the week, using `HOURNAME` and `DAY_WEEKNAME` columns.  

Hour of Day | Accident Count  
  
0 | 1003  
1 | 3364  
1 | 808  
2 | 3613  
2 | 718  
3 | 549  
3 | 4195  
4 | 4256  
4 | 584  
5 | 4619  

![image](https://github.com/user-attachments/assets/530889db-f6d1-4ffe-a72d-1090c54fa575)
Interpretation: Accident frequency peaks during afternoon rush hours (around 3 PM - 6 PM, corresponding to hours 3-6 in the chart which likely represent 24-hour format starting from 0). There are also smaller peaks during morning commute times. Accidents are least frequent in the early morning hours.

#  Accidents by Day of Week  

Day of Week | Accident Count  
  
Sunday | 6327  
Monday | 7502  
Tuesday | 7823  
Wednesday | 8159  
Thursday | 8271  
Friday | 9031  
Saturday | 7632  


![image](https://github.com/user-attachments/assets/1b5566c0-44d6-44d6-8c79-f1e06c7a5071)
Interpretation: Accident counts are generally higher on weekdays, peaking on Friday. Weekends, particularly Sunday, show lower accident frequencies.
  
#  Accidents by Hour and Day of Week (Heatmap)

Hour | Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday  
  
0 | 213 | 129 | 91 | 128 | 114 | 129 | 199  
1 | 618 | 555 | 541 | 585 | 576 | 657 | 640  
2 | 643 | 566 | 589 | 629 | 572 | 693 | 639  
3 | 582 | 639 | 687 | 653 | 742 | 804 | 637  
4 | 473 | 670 | 729 | 766 | 791 | 828 | 583  


![image](https://github.com/user-attachments/assets/414df36e-9a1b-47ec-8b62-6d52daaba2cf)
Interpretation: The heatmap visually confirms the patterns seen in the hourly and weekly charts. The highest concentration of accidents (brighter colors) occurs during weekday afternoon commute hours (approx. 3 PM - 6 PM, Monday-Friday). Early morning hours and weekends show lower frequencies (darker colors).


# Analysis of Accident Hotspots  
This section identifies potential accident hotspots by analyzing accident frequency across different geographical and location-based categories.
  
**- Accidents by Region**  
Region | Accident Count  
  
South (MD, DE, DC, WV, VA, KY, TN, NC, SC, GA, FL, AL, MS, LA, AR, OK, TX) | 28452  
Midwest (OH, IN, IL, MI, WI, MN, ND, SD, NE, IA, MO, KS) | 10390  
West (MT, ID, WA, OR, CA, NV, NM, AZ, UT, CO, WY, AK, HI) | 9287  
Northeast (PA, NJ, NY, NH, VT, RI, MA, ME, CT) | 6616  


![image](https://github.com/user-attachments/assets/113be171-332c-4c29-a877-9372854b5a7a)
Interpretation: The 'South' region reported the highest number of accidents in this dataset, followed by the 'Midwest'.

**- Accidents by Urbanicity**  
  
Urbanicity | Accident Count    
  
Urban Area | 40922  
Rural Area | 13823  


![image](https://github.com/user-attachments/assets/56acb3ea-fa48-4fc1-8add-371091296736)
Interpretation: Accidents occurred much more frequently in 'Urban Areas' compared to 'Rural Areas' according to this dataset.

**- Accidents by Intersection Type**  
  
Intersection Type | Accident Count  
  
Not an Intersection | 30602  
Four-Way Intersection | 13506  
T-Intersection | 5594  
Not Reported | 4502  
Y-Intersection | 171  
Five Point, or More | 160  
Roundabout | 143  
Traffic Circle | 37  
L-Intersection | 22  
Other Intersection Type | 6  
  
![image](https://github.com/user-attachments/assets/8eb48385-ccdd-42be-85d3-02eb0a83f367)
Interpretation: The majority of accidents did not occur at intersections. Among intersection types, 'Four-Way Intersections' had the highest count, followed by 'T-Intersections'.

**- Accidents by Primary Sampling Unit (PSU) - Top 20**  
PSUs often represent geographic areas used in survey sampling. Analyzing counts by PSU can indicate specific areas with high accident frequency.  
  
PSU | Accident Count  
  
38 | 2247  
12 | 1949  
67 | 1837  
28 | 1813  
25 | 1739  
70 | 1604  
83 | 1601  
56 | 1511  
59 | 1428  
48 | 1415  
  

![image](https://github.com/user-attachments/assets/906a5f9c-3b59-43a8-96e4-beff5d1db5c9)
Interpretation: The chart shows the top 20 PSUs with the highest accident counts, pinpointing specific sampling units that experienced more incidents in 2020. Further investigation would be needed to map these PSU codes to actual geographic locations.

# Analysis of Accident Severity  
This section analyzes the maximum severity reported for each accident, using the `MAX_SEVNAME` column.  
  
Severity | Accident Count
  
No Apparent Injury (O) | 24204    
Possible Injury (C) | 12141  
Suspected Minor Injury (B) | 9540  
Suspected Serious Injury (A) | 6270  
Fatal Injury (K) | 1387  
Unknown/Not Reported | 1017  
Injured, Severity Unknown | 166  
No person involved | 19  
Died Prior to Crash* | 1  


![image](https://github.com/user-attachments/assets/bcdcbce7-ddae-4a57-9a13-27af5b5d5b79)
Interpretation: The most common outcome reported was 'No Apparent Injury'. 'Possible Injury' and 'Suspected Minor Injury' follow. Fatal injuries ('Fatal Injury (K)') represent a small fraction of the total accidents in this dataset.
  
# Conclusion  

This analysis of the 2020 US traffic accident sample data revealed several key patterns:    
  
•	Accidents predominantly occur 'On Roadway' and during 'Clear' weather conditions.  
•	Accident frequency peaks during weekday afternoon commute hours (approx. 3 PM - 6 PM), with Friday being the busiest day.  
•	Urban areas experience significantly more accidents than rural areas.  
•	While most accidents do not occur at intersections, four-way intersections are the most common type for intersection-related accidents.  
•	The 'South' region had the highest accident count in this sample.  
•	The majority of accidents resulted in 'No Apparent Injury' or minor injuries, although serious and fatal injuries do occur.    
  
These findings highlight specific conditions, times, and locations associated with higher accident frequencies. Further analysis could explore correlations between these factors (e.g., weather conditions during peak hours, severity by intersection type) to gain deeper insights.

