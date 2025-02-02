---
title: 📈 Data Visualitation
summary: Use popular tools such as Plotly, Mermaid, and data frames.
date: 2024-11-21
authors:
  - admin
tags:
  - Data Visualization
  - Plotly
  - Sales Chart
#image:
  #caption: 'Image credit: [**Unsplash**](https://unsplash.com)'
---

Hugo Blox is designed to give technical content creators a seamless experience. You can focus on the content and Hugo Blox handles the rest.

Use popular tools such as Plotly, Mermaid, and data frames.

## Mid-Semester Assignment for Data Visualization

This assignment is designed to test your skills in creating interactive data visualizations using Plotly.

## Data

The data used for this assignment is a sample dataset that contains information about sales by seller.

## Chart

The chart created for this assignment is a sales chart by seller that displays the sales amount by each seller on each date.

## Code

The code used to create the chart is as follows:
```python
import plotly.graph_objs as go

# Data
date = ['2023-01-01', '2023-01-02', '2023-01-03']
seller_name = ['Seller A', 'Seller B', 'Seller C']
sales_amount = [100, 200, 300]

# Chart
fig = go.Figure(data=[go.Scatter(x=date, y=sales_amount)])
fig.update_layout(title='Sales Chart by Seller', xaxis_title='Date', yaxis_title='Sales Amount')

# Displaying the chart
fig.show()