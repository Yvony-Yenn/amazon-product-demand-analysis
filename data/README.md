# Dataset

The original dataset was collected using the Keepa API and stored in Parquet format.  
The raw data contains multiple product attributes such as pricing, sales rank, reviews, and marketplace information.

During the data preprocessing stage, several columns that were not relevant to the analysis were removed to simplify the dataset and improve modeling efficiency.

### Raw Data Columns

| Column | Description |
|------|-------------|
| ASIN | Unique Amazon product identifier |
| window | Observation window (e.g., 7-day or 28-day interval) |
| date | Observation date |
| SALES_RANK | Amazon sales rank used as a proxy for product demand |
| PRICE | Product listing price |
| BUYBOX_PRICE | Price of the product holding the Buy Box |
| text | Product title or description |
| RATING | Average customer rating |
| REVIEW_COUNT | Number of customer reviews |
| subcat | Product subcategory |
| subcat_aggregated | Aggregated product category |
| New Offer Count: Current | Number of current new offers |
| Count of retrieved live offers: New, FBA | Number of new offers fulfilled by Amazon |
| Count of retrieved live offers: New, FBM | Number of new offers fulfilled by merchants |
| Lightning Deals: Upcoming Deal | Indicator of upcoming Lightning Deals |
| Buy Box: Is FBA | Indicator whether the Buy Box seller uses FBA |
