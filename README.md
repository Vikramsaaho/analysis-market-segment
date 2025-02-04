# analysis-market-segment

analyzing the transaction data to identify the top 3 most profitable products and determine the characteristics of the most loyal customers. Then, I'll summarize my findings. Let me first inspect the data.

The datasets contain the following key information:

Transaction Data (transaction_data):

Contains purchase details, including product number, product name, quantity purchased, total sales, and store information.
LYLTY_CARD_NBR represents a unique customer identifier.
TOT_SALES represents the total amount spent on a transaction.
Customer Purchase Behavior (purchase_behaviour_data):

Maps each customer (LYLTY_CARD_NBR) to a Lifestage (e.g., "Young Singles/Couples", "Older Families") and Premium Customer Segment (e.g., "Premium", "Budget", "Mainstream").
Next Steps
Identify the top 3 most profitable products based on total revenue.
Analyze loyal customers by identifying the most frequent shoppers and their demographic characteristics.
Provide insights into why these loyal customers prefer certain products based on purchasing patterns.
Now, I will proceed with the analysis. ​​

Findings:
Top 3 Most Profitable Products:

Dorito Corn Chips Supreme 380g ($40,352 total sales)
Smiths Crinkle Chip Original Big Bag 380g ($36,367.6 total sales)
Smiths Crinkle Chips Salt & Vinegar 330g ($34,804.2 total sales)
Most Loyal Customer Segment:

Older Families (Budget Buyers) are the most frequent shoppers, with a total of 23,160 purchases.
Hypothesis on Loyal Customer Behavior:
Budget-conscious older families likely prioritize value for money, preferring larger pack sizes (e.g., 330g–380g chips).
They may buy snacks in bulk for family consumption or social gatherings.
Their preference for familiar brands like Doritos and Smiths suggests brand loyalty and trust in classic flavors.

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 264836 entries, 0 to 264835
Data columns (total 8 columns):
 #   Column          Non-Null Count   Dtype  
---  ------          --------------   -----  
 0   DATE            264836 non-null  int64  
 1   STORE_NBR       264836 non-null  int64  
 2   LYLTY_CARD_NBR  264836 non-null  int64  
 3   TXN_ID          264836 non-null  int64  
 4   PROD_NBR        264836 non-null  int64  
 5   PROD_NAME       264836 non-null  object 
 6   PROD_QTY        264836 non-null  int64  
 7   TOT_SALES       264836 non-null  float64
dtypes: float64(1), int64(6), object(1)
memory usage: 16.2+ MB
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 72637 entries, 0 to 72636
Data columns (total 3 columns):
 #   Column            Non-Null Count  Dtype 
---  ------            --------------  ----- 
 0   LYLTY_CARD_NBR    72637 non-null  int64 
 1   LIFESTAGE         72637 non-null  object
 2   PREMIUM_CUSTOMER  72637 non-null  object
dtypes: int64(1), object(2)
memory usage: 1.7+ MB
Result
(None,
     DATE  STORE_NBR  LYLTY_CARD_NBR  TXN_ID  PROD_NBR  \
 0  43390          1            1000       1         5   
 1  43599          1            1307     348        66   
 2  43605          1            1343     383        61   
 3  43329          2            2373     974        69   
 4  43330          2            2426    1038       108   
 
                                   PROD_NAME  PROD_QTY  TOT_SALES  
 0    Natural Chip        Compny SeaSalt175g         2        6.0  
 1                  CCs Nacho Cheese    175g         3        6.3  
 2    Smiths Crinkle Cut  Chips Chicken 170g         2        2.9  
 3    Smiths Chip Thinly  S/Cream&Onion 175g         5       15.0  
 4  Kettle Tortilla ChpsHny&Jlpno Chili 150g         3       13.8  ,
 None,
    LYLTY_CARD_NBR               LIFESTAGE PREMIUM_CUSTOMER
 0            1000   YOUNG SINGLES/COUPLES          Premium
 1            1002   YOUNG SINGLES/COUPLES       Mainstream
 2            1003          YOUNG FAMILIES           Budget
 3            1004   OLDER SINGLES/COUPLES       Mainstream
 4            1005  MIDAGE SINGLES/COUPLES       Mainstream
