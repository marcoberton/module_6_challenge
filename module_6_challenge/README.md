# module_6_challenge
The challenge folder for module 6
# Import the required libraries and dependencies
import pandas as pd
import hvplot.pandas
from pathlib import Path

# Bar plot visual aggregation code
housing_units_by_year.hvplot.bar(
    x='year',
    y='housing_units',
    xlabel='Year',
    ylabel='Housing Units',
    color='purple',
    height=500, 
    width=700,
    ylim=(365000, 385000),
    yformatter='%.0f',
    title='Average Housing Unit Prices Per Year',
    rot=45
)
    
    
# Line plot visual aggregation code (just change a few parameters for the next plot)
prices_square_foot_by_year.hvplot(
    legend=True,
    title='Sale Price Per Square Foot & Average Gross Price -2010 to 2016 - San Francisco',
    x='year',
    xlabel='Year',
    y=['sale_price_sqr_foot', 'gross_rent'],
    value_label='Gross Rent / Sale Price Per Square Foot'
)

# Geoviews plot code
all_neighborhoods_df.hvplot.points(
    x="Lon", 
    y="Lat", 
    geo=True, 
    size="sale_price_sqr_foot",
    scale=1, 
    color="gross_rent", 
    tiles="OSM",
    frame_width=700,
    frame_height=500,
    title="Price per sqr foot v gross rent - San Francisco - 2010 to 2016"
)