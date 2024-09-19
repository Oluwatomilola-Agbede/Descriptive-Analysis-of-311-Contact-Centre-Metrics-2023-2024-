# Portfolio Project:

## Project Description:
Descriptive Analysis of 311 Contact Centre Metrics (2023-2024)

## Project Title: 
Descriptive Analysis of 311 Contact Centre Metrics (2023-2024)

## Objective:
The main objective of this project is to provide a descriptive analysis of the 311 Contact Centre’s activity data in 2023 and 2024. The aim is to pinpoint 
critical performance indicators, analyze tendencies in call volume, service quality, and call drop rates, and provide recommendations for improving organizational 
performance, staffing, and other aspects affecting user satisfaction. 

## Dataset:
The dataset comprises measures of the 311 Contact Centre from January 2023 to 2024. The following key features are included:
Date: When all the data was stored in the organization's database. 
CallsOffered: This refers to the total number of calls received in the contact center on that particular date. 
CallsHandled: This identifies the number of calls the various agents could convert into successful calls. 
CallsAbandoned: The total number of those calls where the customers did not get a chance to speak to any personnel, and they cut the call. 
AverageSpeedofAnswer (ASA): This is the average number of seconds it took for an agent to answer a call to the center. 
ServiceLevel: The fraction of the calls that are responded to within an acceptable time frame concerning the manager. 
BI_ID: A unique record number that can be useful in tracking data from another set or joining it with an existing record. 
## Methodology
### Data Collection and Preparation
 In this step of data collection and preparation, data from the 2023 and 2024 datasets are imported to Python using Pandas from Excel files and 
 merged into the DataFrame containing the year identifier. We then perform data cleaning, wherein we first examine for missing values, remove key 
 observations or legacy values, or apply imputation techniques depending on the research needs. Then, data types are made proper, with the dates in 
 an appropriate `datetime` format, and call metrics numeric to enable calculations on the field. To deal with this issue, data points that might 
 have similar values and thereby affect analysis are eliminated to encourage data credibility. Further, non-working day allowances, which mean days w
 ith extraordinarily low or high call patterns due to weekends and holidays, are also considered. This process covers all bases and leaves the dataset 
 in a clean state and ready for analysis, thus creating a rock-solid foundation with which to work.

Figure 1:

The Output From Data Preparation and Cleaning

As seen from Figure 1, none of the critical columns have any missing values, and therefore, no records would be deleted based on missing data, 
and no data needed to be credited. The cleaned data preview shows daily call center activities, call volumes, call abandon rate, and call service 
performance for several dates in December 2023. The values depicted by CallsOffered and CallsHandled indicate that the call center indeed attends 
to most clients with low call abandoning signs. The AverageSpeedofAnswer and ServiceLevel columns also suggest that the speed is high and the 
quality of answering calls within the defined acceptable time is also good for the center. Also, in the Weekday column, the days of the week are 
highlighted, which will help determine and categorize calls for different days. This kind of output guarantees the quality of the data and is 
suitable for further descriptive analysis.
### Descriptive Analysis
	
 The descriptive statistics step entails computing and analyzing various performance indicators of the 311 Contact Centre for 2023 and 2024, 
 evaluating how the center has been running. First, we find out the total calls offered and total calls handled for the year and see the handling 
 rate, which tells about the efficiency of the number of calls received. The call abandonment rate is expressed daily, monthly, and generally as 
 the number of called-off calls divided by the total number of calls made, pointing to possible Customer drop-off problems. 
 The average speed of answer (ASA) is calculated. Then, the relationship between ASA and abandon rate is analyzed to determine if increased wait 
 time results in increased abandon rate. Service level performance can also be measured by comparing the average service level per year and comparing 
 it to an assumed organizational service level (e.g., 85%). By making this differentiation, it becomes easier to study call handling patterns, 
 call abandonment, and the fluctuating service levels between the two years.
 
Figure 2:

The Descriptive Analysis Outcome.


The output features an analysis of the leading indicators of the 311 Contact Centre for both the years 2023 and 2024. In 2023, it addressed 94. 
27% of the 356,598 calls were offered in 2024, and the average daily abandonment rate increased from 4.62% in 2023 to 6.03% in 2024, reflecting a 
decline in customer retention. There were also fluctuations in monthly abandonment rates by 2024, with higher abandonment in March and July. The 
abandonment rate increased from 4.80% in 2023 to 6.16% in 2024, probably because the average answer speed went from 53.06 seconds in 2023 to 76.86 
seconds in 2024. This increase in wait time is correlated with a high abandonment rate, with correlation values of 0.86 in 2023 and 0.94 in 2024, 
indicating that longer wait times are strongly linked to higher call abandonment.

Furthermore, there was a decline in the average service level from 78.46% in 2023 to 71.26% in 2024, below the assumed target of 85% for both years,
indicating the need to enhance operations. Lastly, the SettingWithCopyWarning warnings imply that the slices of the DataFrame are being modified in 
a way that may lead to issues, suggesting the use of. Loc for safer modifications. 

### Data Visualizations

Figure 3:
Time Series of Calls Offered and Handled

This graph displays the differences in the number of calls offered and handled in 2023 and 2024. The green and purple line corresponds to calls dealt 
with in 2023, while the red and orange dashed line corresponds to the calls offered and handled in 2024. From the chart, it is forecasted that the call 
volume, as well as the handled calls, have been constant throughout 2023, while in the year 2024, the figures go up and down, with some months 
experiencing high call volumes. Further, it is observed that the handling rate has dropped down in 2024 because a smaller quantity of calls has been 
handled compared to calls tried.

Figure 4:
Time Series of Average Speed of Answer

The average answer speed for calls for time series 2023 is in purple, and for time series 2024 is in red. ASA takes the average time an agent takes to 
answer a call to measure the call center's performance. From the graph, it is evident that there are extreme variations in 2023, with some months having 
high ASA and other months having low ASA. As for 2024, we also see that early in the year, there is a deterioration in the response rate and an increase 
in ASA, which means longer wait times.

Figure 5: 
Time Series of Call Abandonment Rates

This time series graph shows the call abandonment rates for 2023 in blue and 2024 in red. The abandonment rate refers to the ratio of the number of calls 
that were not taken before the client hung up. The graph shows that the abandonment rates will fluctuate more frequently in 2023, with inevitable sharp 
fluctuations. In 2024, higher abandonment rates will be presented at more intervals, especially at the beginning of periods, which may suggest operational problems.

Figure 6:
Monthly Service Level Achievements

This graph, presented as a bar chart, indicates the service level performance over the months of 2023 and the predicted performance in the months of 2024. The graph 
shows the number of calls responded to within the required call duration. The green dashed line shows the desired service level of 85%. The left side 
of the figure compares the service level 2023 by the blue color bars, and the right side reflects the performance of 2024 by the red color bars. The chart shows that 
the service levels for 2023 and 2024 are slightly below the target level and much lower in 2024 compared to 2023.

Figure 7:
Call Handling Efficiency by Month

This bar chart demonstrates the relative monthly call handling in 2023 (green bars) and 2024 (yellow bars). Call handling efficiency is the number of calls handled 
divided by the number of calls offered. The chart also provides information about handling efficiencies in 2023, in which all the values are almost equal to 1, 
meaning nearly perfect efficiency. Nevertheless, it is evident that from January 2024, the efficiency reduced, implying that the number of effectively managed calls 
was lower than the number of calls offered.

Figure 8:
Distribution of Calls by Outcome (Handled vs. Abandoned)


The left pie chart represents the record of calls the company successfully managed compared to the calls dropped in 2023. The green section represents 95.2% of 
the total calls managed to be tended to, while the red portion, or 4.8%, belongs to the disconnected calls before being responded to. This shows that in 2023, the 
contact center can respond to most calls made to the contact center, and only a tiny percentage of the calls were abandoned. The right pie chart illustrates the 
distribution of the calls made in 2024. The purple area represents 93.8% of the managed calls, and the orange portion is 6.2%. Thus, there is a slight performance 
deterioration, with more customers being disconnected before they are helped in 2024 compared to the number of disconnected calls in 2023.

Figure 9
Heatmap for Peak Call Times by Day of the Week


This heatmap visualizes the call volume for 2023 with axes displaying the day of the week and the hour of the day. The call volume is also represented by the intensity
of blue, with a higher intensity of blue representing high volume and a lower intensity representing low volume. The chart represents the call volume being almost uniform
across the days of a week, with some fluctuations depending on the hours, indicating relatively unchanging call traffic during the week. The 2024 heatmap focuses on 
the call volume for 2024 and includes the day of the week and the hour of the day. Darker red shades represent higher call volume, while lighter shades of red represent 
lower call volume. Like the 2023 heatmap, call activity is evenly distributed throughout the week, although it may differ from 2023 depending on the hours or days of 
the week.

Figure 10:
High Call Volume Days

The left column of this table shows the days in 2023 when call volume exceeded the mentioned number, which is in the top 10% of the most busy days. This then demonstrates 
the number of calls offered on the high volume day in line with the date in the table. Some days, for example, in late July, they had many calls compared to others, 
showing they had high operations. As with the 2023 table, this table presents all days in 2024 during which the call volume exceeded the 90th percentile. It also i
ncorporates months such as January and July, which experienced a high recording of call traffic in 2024, implying possible seasonal or event-triggered occasions.

Figure 11:
Service Performance by Hour

This line graph indicates the average service level performance per hour, and for 2024, the hour is represented in red. The service level shows a spike for the first hour 
between midnight and 1 AM and is very low for all other hours of the day, suggesting that the contact center may be overstaffed or more productive during off-peak hours, 
but cannot sustain the performance for the rest of the shift.

## Key Insights and Findings
Comparing the 311 Contact Centre performance data for 2023 and 2024, it is possible to identify differences in efficiency indicators, including the rate of call handling, 
abandon rates, and service levels. As reflected in the center's outcomes, it worked efficiently and dealt with 95% of the tasks in 2023. As depicted in the distribution of 
calls, 2% of the total calls are offered. The call handling efficiency for the messages remained high throughout the year, not declining below 98% in any of the months. M
oreover, the service level for 2023 was moderate, fluctuating much below the 85% target in many of the months of the year, and abandonment rates were relatively low, with an
average abandonment rate of 4. 8%. These metrics show that this contact center in 2023 is up and running with little disturbances and strong daily call traffic management. 

The situation is worse for the year 2024 when organizational performance has taken a downward trend. Orchestration-related parameters showed trends consistent with the call 
volumes; ABS elevation call handling efficiency was reduced compared to actual values for 2023, with an efficiency below 90% in several months, meaning fewer calls were being handled compared to what was offered. The abandonment rate was also brought up to 6. The abandon rate of the queue, indicated that 2% of customers were hanging up before being answered. This increase in call abandonment can be attributed to a significant shift in the average speed of answer (ASA) which shows that the time clients have to wait to be answered in 2024 is more than that of 2023. From the analysis of ASA, it is clear that the response time has gradually increased over the years, which is very unprofitable for businesses. Further, the 2024 service level was also below the target consistently noting that the company needed help in achieving its operational targets. 
The heat maps and high call volume day analysis indicate that some months, especially January-February and July-August, have a high call volume number for 2023/2024. 
Nevertheless, it turned out that the strength of the contact center in dealing with such fluctuating call influxes was better in 2023, as illustrated by low effects on handling and abandonment ratios. Conversely, 2024 recorded fluctuating pattern with higher call traffic requiring higher call handling efficiency accompanied by reduced call abandonments. These findings imply that technical factors, which include deficiency in staff number or inefficient distribution of calls during busy period, could have gotten worse in 2024 to affect the general decline in performance. With the current trends, although the volume of call traffic and call time is decreasing, the number of answered calls is also declining, meaning that staffing levels during popular operational periods, or improved call handling technologies, would be required to return the center to the levels that it delivered in 2023.

## Recommendations

For better management of the call volume and enhancement of call handling time for a 311 Contact Centre, the most crucial factor that should be considered is call staffing
during peak times, which was also revealed by high call volume analysis. The peak months were January and July, and it was established that these were the months that saw 
dips in handling efficiency and a rise in abandon rate in 2024. This way, the center can decrease the average speed of answer (ASA) and guarantee that more calls are taken
as soon as possible to reduce customer anger and disconnecting. 

Also, the contact center should ensure that call routing technology is improved and that automated means are adopted for handling high volumes of calls. This correlation 
depicts a significant observation where the abandonment rates in 2024 are associated with prolonged ASA times, suggesting that how calls are handled and directed was 
ineffective. Measures such as using better call routing techniques, having effective call queues, or introducing automated customer service options help decrease the 
contact time to a minimum and ensure that the tasks are shared well across the organization while increasing the overall service quality. 

Finally, there is a need for the contact center to reduce the service level expectation achieved as well as the real-time reporting and performance measures. The analysis 
shows that the service level remained below the targeted 85 % in both 2023 and 2024. In this case, it will be helpful that the center does not keep this as a fixed goal 
but evaluates the organizational performance and sets realistic goals that it can quickly meet. Real-time monitoring tools can also identify slow-performing areas so that 
corrective measures can be instituted before the impact on customers is felt.
