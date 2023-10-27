# Power BI Dashboard of PwC Company's Call Center Data

This Power BI project focuses on analyzing and visualizing call center data from PwC Company, which comprises a dataset with 5000 records. The dataset includes the following columns: Agent, Date, Time, Topic, Answered (Y/N), Resolved, Speed of Answer in seconds, Average Talk Duration, and Satisfaction Rating. The primary objective of this project is to provide valuable insights into the performance and efficiency of PwC's call center operations, enabling data-driven decision-making and enhancing customer service.

## Key DAX Measures Utilized:

### Total Calls:
Calculation: COUNT('Call Center Data'[Call Id])
Purpose: This measure counts the total number of calls in the dataset, providing an overview of call volume.

### Total Answered Calls:
Calculation: CALCULATE([Total Calls], 'Call Center Data'[Answered (Y/N)] = "Y")
Purpose: This measure calculates the total number of calls that were answered (Answered (Y/N) = "Y"), helping evaluate call center responsiveness.

### Total Rejected Calls:
Calculation: CALCULATE([Total Calls], 'Call Center Data'[Answered (Y/N)] = "N")
Purpose: This measure determines the total number of calls that were not answered (Answered (Y/N) = "N").

### Total Resolved Calls:
Calculation: CALCULATE([Total Calls], 'Call Center Data'[Resolved] = "Y")
Purpose: This measure calculates the total number of calls that were successfully resolved, providing insights into issue resolution rates.

### Total Unresolved Calls:
Calculation: CALCULATE([Total Calls], 'Call Center Data'[Resolved] = "N")
Purpose: This measure quantifies the total number of calls that remain unresolved, helping identify areas that require attention.

### Average of Average Call Duration:
Calculation: AVERAGE('Call Center Data'[AvgTalkDuration in Second])
Purpose: This measure computes the average of the average call durations, aiding in understanding the typical duration of calls handled by the call center agents.

### Average of Satisfaction Rating:
Calculation: AVERAGE('Call Center Data'[Satisfaction rating])
Purpose: This measure calculates the average satisfaction rating provided by customers, allowing for the assessment of customer satisfaction levels.

### Average Speed of Answer in Seconds:
Calculation: AVERAGE('Call Center Data'[Speed of answer in seconds])
Purpose: This measure determines the average time it takes for calls to be answered, providing insights into call center efficiency and responsiveness.

The Power BI dashboard created as part of this project will feature various visualizations, including charts, graphs, and tables, to effectively communicate the findings from these DAX measures. Users of the dashboard will be able to explore and interact with the data, gain actionable insights, and make informed decisions to optimize PwC's call center operations and enhance customer service.

By leveraging the power of Power BI and DAX measures, this project aims to provide PwC with a comprehensive view of its call center performance and help identify opportunities for improvement, ultimately leading to better customer service and increased operational efficiency.
