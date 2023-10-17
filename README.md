# Assignment5
**Exploration of In-Vehicle Coupon Recommendations**
Origin of Data: https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation
  Data was surveyed from drivers that were given the option of accepting or rejecting coupons.
Our exploration of the data begins in the section titled **Problems**.

**First, clean up the data.**
For all coupon types, the acceptance rate was 56.84% The greatest number of coupons were accepted on days when the temperature was 80F. 
The least amount of coupons were accepted in 30F temperatures.

**Bar Coupons**
Per the instructions of the assignment, we first samples coupons specific to bar coupons which resulted in 2017 entries.
When only considering bar coupons, the acceptance rate overall was 41%.
With the incorporation of different variables, we begin to see which populations were more or less likely to accept coupons.
Those who went to the bar >3x a month were 36.40% more likely to accept the coupon than those who went less.
Those who went to the bar >1x a month and >25 years old were 26.91% more likely to accept the coupon than those who went to bars less and <25 years old.
Those who went to the bar >1x a month, without kid(s), and not working in farming, fishing, or forestry were 22.89% more likely to accept the coupon than their counterparts.
Passengers who go to the bar >1x a month, without kid(s), and not widowed have a coupon acceptance rate of 67.33%.
Passengers who go to the bar >1x a month and <30 years old have a coupon acceptance rate of 68.70%
Passengers who go <$20 restaurants more than 4x a month and earn less than $50K have a coupon acceptance rate of 45.39%

**Conclusion**
Several factors were examined regarding the passengers who accepted Bar coupons. 
Some factors examined were age, bar visiting frequency, occupation, age, income, and the presence of children. 
According to the results of the analysis of the bar coupons, it can be concluded that with increased age, higher frequency of going to bars, and being without children, drivers were more likely to accept coupons. 
The organization should continue to offer coupons to drivers over 25 years of age who frequent bars regularly and earn higher incomes because these groups have exhibited the highest acceptance rates.
Some parameters that were looked at but require further investigation are occupation, marital status, and income level.
Through further investigation of these variables, we have identified groups with higher acceptance rates.
However, I think it would be worthwhile to tap into populations that have low acceptance rates to increase the customer base.
For drivers with children, who have exhibited lower acceptance rates, bars can offer promotions on food as well to enhance the experience for the whole family that would be appropriate for all ages.

**Independent Investigation**
I chose to examine the effect of different variables on Coffee House coupons since I am an avid coffee drinker.
There are 3996 entries related to coffee house coupons.
I was able to explore the data using the info, head, describe, and corr functions to get a better idea of the data I was working with. 
Next, I created a multitude of subplots to examine the histographs of each variable and how it related to coupon acceptance rates.
By examining these visualizations, it was very striking to see how different variables strongly affected acceptance rates such as the destination of the driver.
A few examples are destination, weather, distance to the business, time of day, and frequency of coffee house visits.
With the current model, **49.92%** of coffee house coupons are accepted.
From the results of the histograms, I decided to focus on several variables: time, temperature, weather, destination, and directionality.
Acceptance of coupons for specific temperatures and weather conditions were so drastic, I wanted to control for those variables.
The dataset was queried for 55F and 80F temperatures and sunny weather.

**One of the main variables I looked at was time which I separated into 3 categories.**
Peak Viewing = times with the greatest of amount of coupons viewed, accepted and rejected combined, 7AM, 10AM, 2PM, 6PM
Peak Acceptance = times with the highest acceptance rates, 10AM & 2PM
Peak Rejection = times with the highest rejection rates, 7AM, 6PM, 10PM
In my analysis, I found that during peak acceptance times (10AM & 2PM), 16.88% more drivers accepted the coupon compared to peak rejection times at 7AM, 6PM, and 10PM.
During peak times of viewing coupons (7AM, 10AM, 2PM, and 6PM), 9.70% less passengers accepted the coupon compared to peak acceptance times (10AM, 2PM).
**Directionality**
During times when the most coupons were viewed, drivers were 4.11% more likely to accept a coupon if traveling in the same direction as the business than the opposite direction.
**Destination**
When exploring drivers under the same conditions but in consideration of destination, those who had no urgent destination were 20.16% more likely to accept a coupon than those traveling home and 15.48% more likely to accept a coupon than those traveling to work.

**Conclusion**
In this examination of the data, it is clear that timing of the coupon release is an important factor to consider. 
The peak times of acceptance were 10AM and 2PM which would help direct our efforts to increasing coupon exposure during those times until we find a rate where acceptance plateaus.
When looking at the peak viewing times for coupons, it doesn't seem that expanding the time from 7AM to 6PM is beneficial to coffee house offers since there are 9.7% less customers interested than at 10AM & 2PM.
When looking at the directionality of the drivers, the improvement of acceptance rate was not significant. 
This tells me that coupons are not distributed based on directionality which may be a missed opportunity for businesses to target drivers that are headed towards the business.
Finally, the destination of the driver was a significant factor in acceptance rates. 
Drivers with no urgent destination were very successful for coffee house coupons. 
Areas for further examination are coupon offerings during other times such as 7AM and 6PM.
One would think that 7AM would be a popular time for coffee but I think it would be worthy to examine other offerings such as curbside pick up or breakfast offerings.
If there is a way to determine the direction drivers are headed, it would might be worthwhile to focus offerings to drivers coming in the same direction.
Finally, the greatest opportunity for business and coupon expansion would be for those not going to work or home.
If our model can determine those who have no urgency, coupons can be directed to these drivers for the highest rate of success. 
Some areas for further exploration might be occupation and education level because unemployed drivers and students were some of the highest coupon users along with those with some college and bachelor degrees.
I think it would be useful to look at the demographics of the areas such as near a university and a younger community would provide direction and how much to invest a certain type of coupon in a geographical area.
