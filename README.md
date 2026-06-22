# Walmart Sales Analysis

I picked up this dataset from Kaggle and just wanted to dig into it and see what the numbers were actually saying. No fancy pipeline, no overengineered code  just a straightforward analysis to understand how Walmart's sales behave across different stores, time periods, and economic conditions.

---

## Why Walmart?

Walmart is one of the largest retailers in the world, and their sales data is actually really interesting to work with because it captures so much more than just revenue. You've got external factors like fuel prices, inflation, unemployment — things that directly affect how people spend money. I wanted to see if any of that actually shows up in the data.

---

## What I Did

I started with a single CSV containing weekly sales for 45 Walmart stores from 2010 to 2012. First pass was just cleaning — fixing date formats, checking for nulls, getting rid of duplicates. Nothing was badly broken, which was nice.

Then I just started asking questions.

Which stores are actually making the most money? Does it matter if it's a holiday week? What does November look like compared to January? Does the price of gas affect how much people spend at Walmart?

For each question I made a chart, looked at it, and wrote down what I thought it meant from a business perspective. That's basically the whole notebook.

---

## What I Found

A few things stood out to me:

- A small number of stores are responsible for a huge portion of total revenue. Classic Pareto situation.
- Holiday weeks are noticeably higher than regular weeks. Not a surprise, but it's good to see it confirmed in the data.
- November and December are the peak months every single year without exception. January is always the lowest.
- When inflation goes up, Walmart's sales don't really suffer — if anything there's a slight uptick. Makes sense when you think about it. People start looking for cheaper options and Walmart is exactly that.
- Temperature and fuel prices don't have a strong direct relationship with overall sales. The correlations are there but they're weak.

---

## Dataset

Walmart Store Sales data from Kaggle — 6,435 rows, 45 stores, weekly from 2010 to 2012.

Columns: Store, Date, Weekly_Sales, Holiday_Flag, Temperature, Fuel_Price, CPI, Unemployment

---

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook walmart_analysis.ipynb
```

---

## What's Next

Feature engineering and a forecasting model. The data is clean and saved as `cleaned_walmart_sales.csv` — ready to go whenever I pick this back up.
