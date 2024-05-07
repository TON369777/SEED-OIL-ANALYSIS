# SEED-OIL-ANALYSIS

## OVERVIEW


## DATA
Ingredients information of ~14 000 products were scraped from the Coles Supermarket website. 

**Web Crawl and Scrape**

A crawler program was written in Python to crawl and scrape the Coles website for all food products and ingredients information. The program would crawl through each of the product categories, obtain the individual product URLs and then individual product ingredients information scraped. Of note is that the program was interrupted at times and so the program had to be restarted many times. The raw data that was scraped was ultimately split into multiple files.

**Data Cleansing and Formatting**

Before any analysis could take place, some data cleansing and formatting was required.

1) Baby Products consists of both food and non food items. Non food items were filtered out before analysis.
2) Additional columns were added to indicate presence of specific seed oil types. 1 indicates Yes, 0 indicates No
![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/c3e992ce-bfd4-4f81-9dc3-00f3b9de3265)
3) Final additional column was added to indicated an overall presence of seed oil/s in the product. As long as there was at least 1 indication of 1 value in preceding additional columns, this final column would indicate 1 for Yes.
![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/c1168f68-f462-44e5-8b56-cd5c59d0efcb)![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/e4549483-44a0-4427-a985-d51115b3037a)

## ANALYSIS
Data Analysis was completed using Python Pandas. Points of interest include:
1) Counts of all products and across all product categories
2) Counts of products with seed oils + proportion across all product categories
3) Instances of seed oils across all products and their individual categories

## VISUALISATION
Dashboard was also created in PowerBI to visualise data allowing interested users to examine trends about seed oils in food products at COLES.

1) Main Page - number of products with seed oils and % of all products
2) Seed Oils - information about the makeup of specific seed oils across all product types
3) Grid - Users can browse/ look up individual product names and if they possess seed oils

Product category filter can be used to filter desired category/categories.

![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/3de64409-9edf-486a-80dc-58af240dd3d2)
![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/9c62f060-bfe5-42fe-9f31-af486a2eea68)
![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/ecb72c38-f85e-4781-8889-c1f9ee048c1e)


## INSIGHTS
