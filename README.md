### Marketing Campaign
Marketing Campaign data of Maven Marketing including customer profiles, product preferences, marketing campaigns successes/failures
and the performances of the various channels. 

### Questions to be Answered
- Are there null values?
- What factors are significantly related to web purchases?
- Which marketing campaign is the most successful?
- Which products are performing best?
- Which channels are uderperforming?

### Process Used in Answering the Questions
- There were blank rows in the Income column. I opened the data in excel initially and filled the blank cells using find and select.
- Created a new column(Age) using the preexisting column (year of birth of customers).

- Now to answer the second question, I plotted a scatter plot using four quantitative variables against the `NumWebPurchases` column.
The scatter plot could not give a clear indication of the relationship between the variables and the web purchases so I went ahead to
to find the p_value using linregress.
The p_values for the various variables that is `Income`, `Age`, `Number of Kids at home`, `Number of Teen at home` and `Number of web visits per month` rejected
the null hypothesis. Therefore the conclusion that all those variables are significantly relatd to Web Purchases(Number of purchases
made through the company's website was made. 
For categorical variables(Marital status and Country), I used bar charts for the visualization and f_oneway to find the P-values. 
Both variables had p_values greater than the threshold(0.05) hence accepting the null hypothesis that those variables are not 
significantly related to the number of web purchases.

- On to the third question, the most successful campaign was the `Fourth Campaign`. The number of accepted offers for this campaign
was 167 against 30 accepted offers from the `Second Campaign` which was the worst campaign. Using value counts to sum up the
rejected and accepted offers and then plotting to visually see the difference. 

- To answer the question, what products is performing best, I created a dataframe with the products and total amount spent on them
over the past two years. I sorted the sum of the purchases and plotted them using a bar chart. The products that are performing best 
are `Wine` and `Meat` products. The least performing product is Fruits.

- The underperforming channels are `NumdealsPurchases` and `NumCatalogPurchases`. The total number of purchases made using a discount(NumdealsPurchases) and number 
of purchases made using a catalogue( NumCatalogPurchases) are `5208` and `5963` respectively. I used the same process used in finding the best performing product.
