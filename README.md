# ML-AI-Berkeley
All tasks associated with ML/AI Online Course hosted by Berkeley Engineering College
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under $20), coffee houses, carry out & take away, bar, and more expensive restaurants ($20 - $50).

The following analyses are categorized based on the five types of coupons offered; Restaurants where the average cost per person is below 20$, Coffee House, Carry out & Take away, Bar, and Restaurants where the average cost ranged from 20-50$.

I began by filtering the dataset to include only the coupons that were accepted and then by each category of coupon. The objective behind this initial filtering was to make the analyses very specific and allow for the drawing of actionable conclusions. I wanted to see what were the most common situations which prompted the acceptance of coupons, and thusly disregarded rows of the dataframe were the coupons were not acted upon.
Given the categorical nature of the many of the dataframe’s columns, it was challenging to get any clues on where to begin searching for relationships with a heatmap as can be observed in the below Heatmap figure. So I started thinking about the human element and what variables could prompt someone to accept a coupon for a particular establishment.

5.1 Heatmap


Thinking from a human perspective, I started to brainstorm what are the factors that prompt someone to get a cup of coffee, pastry, or spend time at a café. The first was weather, so I began by comparing the acceptance rate of coupons separated by weather. The Histogram displayed an equal number of total rejected and accepted coupons and the distribution of weather was also identical. I was able to rule that the weather has no impact on the acceptance rate of coupons.

Activity 5.1 Coffee House coupon accepted vs weather


Following that I tried to inspect the income data for coupons accepted for Coffee Houses, and stratified by frequency of visits. This displayed a bimodal distribution peaking at the 43K and 100K income levels. I noticed that those under the income level of 63K per annum were by the far greatest enthusiasts of Coffee House coupons. Probably for good reason since those with income below the median will want to save money wherever they can. Those of an income level of 100K enjoyed accepting Coffee House coupons as well. This is probably since they had enough disposable income to indulge on Coffee Houses, but not enough to disregard potential savings opportunities where they could.

Activity 5.1 Coffee House coupon accepted vs income levels


The next coupon category is for cheap restaurants. I started to think that maybe there was a time component to any patterns in this filtered data. It turns out that coupon acceptance peaked from 6PM to 10PM during times when the temperature was around 80 degreed Fahrenheit. A reasonable assumption from this is that people were picking up dinner after work or going out friends or family in the evenings. I would love to do a deeper dive into this based on destination, passengers, and direction. 

Actvity 5.1 Cheap Restaurants Histogram


Going back to my college days and time living alone, I brainstormed the age groups of people that would be willing to accept a coupon for Carry Out/Take Out. My line of thought struck gold and a very clear pattern emerged when plotting a histogram of accepted coupons with bins of Age Groups and stratified by frequency of bar visits. It seems that once people graduated college, got their first jobs and their own income; they began to enjoy their newfound freedom by getting take out frequently. The number went down as people got older, probably because people started meal prepping more and budgeting their income for other expenses such as a home, family, or other investments. The coupon acceptance increased again at the 50 and above age group, possibly because the elderly have had their kids move out and have a newfound freedom to explore and/or no energy/interest to cook for themselves at home. 
I also wanted to see if the frequency of visiting bars had a relationship to impulsive take out orders, but the distribution of bar visitation frequency appears to be slightly even across all age group categories.

Activity 5.1 Take Out coupon accepted vs age group and bar frequency


