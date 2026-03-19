# Practical Application Assignment 5.1 – Will the Customer Accept the Coupon?

This project focuses on understanding what influences a customer’s decision to accept or reject a driving coupon. Using data visualization and probability based insights, the goal was to identify patterns that separate customers who accept coupons from those who don’t.

The dataset used for this analysis can be found here:  
[Link to Coupons Dataset](/coupons.csv)

The analysis was carried out in Python using commonly used data science libraries such as pandas, seaborn, matplotlib, numpy, and sweetviz.  
All code, visualizations, and detailed observations are available in the Jupyter Notebook below:  
[Link to Jupyter Notebook](/prompt.ipynb)

---

## Exploratory Data Analysis

To get an initial understanding of the dataset, the SweetViz library was used to generate an automated exploratory report:  
[Link to SweetViz Report](/SWEETVIZ_REPORT.html)

### Data Quality Observations

#### Missing Data
The `car` column had nearly 99% missing values, making it ineffective for analysis, so it was removed. Other columns had very minimal missing data (less than 2%), which was not significant enough to impact the analysis.

#### Duplicate Data
There were 74 duplicate rows. Since this is survey data, duplicates can naturally occur, and every response was considered valuable. Therefore, duplicates were retained.

---

## General Data Visualizations

![Coupon Type Distribution](/images/CouponTypeDist.png)

![Temperature Distribution](/images/TempDist.png)

---

## Key Insights

### Overall
- About **57%** of coupons were accepted.

### Bar Coupon Insights
- Overall acceptance rate: **41%**
- Customers who visit bars **3 or fewer times/month**: **37% acceptance**
- Customers who visit bars **more than 3 times/month**: **76% acceptance**
- Drivers visiting bars more than once/month and aged over 25: **70%**
- Drivers visiting bars frequently, with non-kid passengers and non-manual occupations: **~71%**
- Drivers not widowed and frequent bar visitors: **~71%**
- Drivers under 30 who visit bars often: **72%**
- Lower-income drivers (<50K) who frequently visit cheap restaurants: **45%**

---

## Hypotheses

Based on the patterns observed, several trends emerge:

- **Frequent Bar Visitors**  
  Customers who regularly go to bars are far more likely to accept bar-related coupons. This suggests familiarity and relevance strongly influence acceptance.

- **Age Influence**  
  Younger drivers, especially those under 30, tend to accept bar coupons more often. This may reflect lifestyle preferences and social habits.

- **Marital Status & Occupation**  
  Individuals who are not widowed and those outside certain labor-intensive occupations appear more likely to engage with these coupons, possibly due to lifestyle flexibility or social behavior.

- **Income & Spending Behavior**  
  Customers with lower income but frequent dining habits show moderate acceptance rates, indicating price sensitivity and value-driven decisions.

- **General Population Behavior**  
  Drivers who don’t fall into these specific groups are less likely to accept coupons, suggesting that targeting matters significantly.

---

## Independent Investigation – Carry Out & Take Away Coupon Declines

This section explores who is more likely to *decline* carry-out and take-away coupons.

![Declines by Age](/images/CouponsDeclineByAge.png)

### Age
Drivers aged **21 and 26** are the most likely to decline these coupons, each contributing to about 20% of total declines. This points toward a noticeable trend among younger adults.

![Declines by Marital Status](/images/CouponsDeclineByMaritalStatus.png)

### Marital Status
- Married individuals: ~40% of declines  
- Single individuals: ~37%  

Marital status appears to play a meaningful role in coupon rejection behavior.

![Declines by Education](/images/CouponsDeclineByEducation.png)

### Education
- Bachelor’s degree holders: ~37% of declines  
- Some college (no degree): ~30%  

Higher education levels seem to correlate with a greater likelihood of declining these coupons.

---

## Recommended Next Steps

To build on these findings, the following steps are recommended:

- **Segmentation Analysis**  
  Dive deeper into customer segments by combining variables like time of day, weather, and location to uncover more detailed behavioral patterns.

- **Predictive Modeling**  
  Develop machine learning models to predict coupon acceptance based on user demographics and behavior.

- **A/B Testing**  
  Experiment with different coupon designs, messaging, and offers to identify what resonates best with different audiences.

- **Economic Impact Analysis**  
  Measure how coupon campaigns affect business metrics like revenue, retention, and customer engagement.

- **Competitive Analysis**  
  Study how competitors are leveraging similar promotions to identify gaps and opportunities.

- **Multi-Channel Integration**  
  Combine coupon campaigns with channels like email, social media, and app notifications to improve reach and effectiveness.
