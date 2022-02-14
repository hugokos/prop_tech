# PropTech

This Jupyter Notebook is a property tech application that created visualizations for the San Francisco property market

---

## Technologies

Project uses:

[Pandas](https://pandas.pydata.org/)

[pathlib](https://docs.python.org/3/library/pathlib.html)

[hvplot](https://hvplot.holoviz.org/)



---

## Installation Guide

Run this program in Jupyter notebook and have a hvplot installed



---

## Usage

Utilize Jupyter Labs to interact with the software program

!["Jupyter Labs Example"](https://miro.medium.com/max/955/1*mXGu0MeYgnUkyR9ybVlQpg.png)

**Key example code for hvPlot GeoViews map**
```
# Call the dropna function to remove any neighborhoods that do not have data
all_neighborhoods_df = all_neighborhoods_df.reset_index().dropna()

# Rename the "index" column as "Neighborhood" for use in the Visualization
all_neighborhoods_df = all_neighborhoods_df.rename(columns={"index": "Neighborhood"})

# Review the resulting DataFrame
display(all_neighborhoods_df.head())
display(all_neighborhoods_df.tail())

all_neighborhoods_df.hvplot.points(
    'Lon', 
    'Lat', 
    geo=True,
    size="sale_price_sqr_foot",
    color="gross_rent",
    frame_width=700,
    frame_height=500,
    title="Interactive Neighborhood Map: Gross Rent and Sale Price per SqFt"
)
```

---

## Contributors

Hugo Kostelni

---

## License

Open Source