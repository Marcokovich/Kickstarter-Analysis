# Kickstarter-Analysis
## Overview of Project
### Background
Louise's play Fever came close to its Kickstarter fundraising goal in a short time. To see how her campaign did in relation to others, a data set was acquired of other Kickstarter attempts. The data is has outside info such as the name, description, backers, and staff opinions. It also has more important data pertaining to its success such as goal, amount pledged, outcome, launch date, deadline, categories, and subcategories.
### Purpose
Using the Data from Kickstarter the goal of this project is to visualize the outcomes of these campaigns based on launch date and fundraising goals.
## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
- The months of May and June have the highest percentage of successes.
- The months of December and October have the highest percentage of failures.
- The month of January has the higher percentage of cancellations.
![Theater_Outcomes_Based_on_Launch_Date](https://user-images.githubusercontent.com/71575748/146625569-4d2d5c5d-d718-4adf-990a-0dd75130f915.png)
- We can see an upward trend in total campaigns towards May and June and see a downward trend for the rest of the year.
- It can also be observed that there is a peak in failures in October.
### Analysis of Outcomes Based on Goals
- Goals less than 1000 have the higher percentage of successes.
- Goals over 10000 become less common, and even likely to show up past the 25000 mark.
- This coincides with a decrease in success rates.
- A lower portion of the sample in theis regards makes it hard to determine if this is a general trend or not.
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/71575748/146625656-36d59e9c-af95-4c01-9961-1caf467460ef.png)
- A downward trend of successes can be seen from the lower goals to the higher goals until the 35000 to 45000 range where an increase of successes can be observed.
- However, it must be kept in mind that the sample size is very limited at these ranges so it may not be able to speak for a more general approach.
### Challenges and Difficulties Encountered
- The dates in the data set were in epoch time, which is unable to be graphed in a reasonable fashion.
  - This was alleviated by decoding the epoch into the Gregorian date using the line. The Month was extracted after.
     - =DATE(YEAR(I2 / 86400+25569),MONTH(I2 / 86400+25569),DAY(I2 / 86400+25569))
- The ranges of the goals were inputted manually, while not particularly challenging it was time consuming to make the table without being able to use macros to fill the different ranges. However, by locking data columns it was possible to drag the countifs, only having the manually change the criteria based on success/failure/cancelled.
## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
   - Campaign density increases during early summer (Particularly May and June), there is also when there are the higher ratio of successes to failures.
     - This can likely be attributed to the time of year being more ideal for production since working in winter conditions can be more difficult.
   - The opposite can be observed in projects launched towards the end of the year, with October and December having the lowest.
     - This can be attributed to a decrease in donors likely due to holiday spending.
- What can you conclude about the Outcomes based on Goals?
   - I don't think its much of a surprise, but campaigns with lower goals have a much higher success rate than those with more goals. It is likely due to how much money that needs to be collected, or that donors favor more reasonable campaigns.
- What are some limitations of this dataset?
   - The higher goals don't have as many observations i.e. the range $45000 to $49999 only has 1 observation, so any analysis may be a bit biased as there is only 1 observation to work with.
- What are some other possible tables and/or graphs that we could create?
   - Graph the success rate of the different categories or subcategories to see if plays perform better or worse than other subcategoreis in theater. Alternatively we can see if     theater performs better than other parent categories.
   - We could also see if the spotlight or staff picks had any impact on the success of the projects relative to the goals or dates.
