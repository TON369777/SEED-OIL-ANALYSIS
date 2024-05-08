## OVERVIEW

This analysis examines the prevalance of seed oils in our food supply by examining the ingredient contents of food products offered at one of Australia's biggest supermarket chains, Coles. For health conscious individuals looking to avoid consumption of seed oils, this study would be of great interest to find out just how widespread seed oils are used and what products to avoid.

The vegetable oil industry is a multi billion dollar industry worth $232 billion globally (2020) and $3.45 billion in Australia alone (2016-2017) with seed oils making up most of the market including canola, soybean and sunflower. The interesting thing of note is that whilst seed oils are classified under vegetable oils, the oil itself has nothing to do with vegetables and is instead produced from seeds under a very intensive industrial process that would otherwise not exist without this process. Health conscious individuals are concerned with the long term health effects of consuming seed oils for this reason and many others.

a) Manufacters of seed oils have gone to lengths to market seed oils under vegetable oils, even as far as not even being required to name the specific seed oil. As an example, this 'Crisco Vegetable Blended Oil' only lists 'Vegetable Oil' as the ingredient.

![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/41ec3885-00f4-4287-bbd8-7b5c4c77f986) ![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/034d8b09-7b5c-40b6-a187-cf24d07c04d7)

Seed oil usage were used other purposes other than human consumption.

b) Procter & Gamble was one of the first companies to market and sell a form of seed oil. Originally, their production of cottenseed oil was to be used for soap however through technological developments around hydrogenation produced what was then accepted as food consumable oil under the name of Crisco in 1911. This product contained high levels of trans fats later thought to be linked in increasing rates of heart disease. P&G have since altered the Crisco product to reduce levels of trans fat.

c) Canola oil is a form of seed oil made from the rapeseed flower. There is no flower called 'canola' and instead stands for 'Canadian oil, low acid'. Rapeseed oil was mainly used for biodiesel fuel purposes such as powering motor vehicles and was not suitable for human consumption due to high levels of erucic acid which in laboratory studies shown to be damaging to cardiac muscle. Canola oil is produced from rapeseed varieties bred for low erucic acid values with government regulation in US and the EU allowing up to 2% erucic acid by weight. Canola oil is one of the most consumed seed oil in Australia.

d) Seed oils have high levels of polyunsaturated fats which have been marketed as being "good" and "healthy" fats by manufacturers of seed oils and organisations linked to heart health and disease research (who are funded by the very same manufacturers of seed oils) whilst also at the same time demonising saturated fats often found in butter, ghee and animal fat products such as lard, tallow for increased rates of heart disease. By the way,  humans have consumed butter and animal fats long before the existence of industrial scaled production of seed oils. Could this negative characterisation of butter and animal fats be for the purposes of creating a market for seed oils that would otherwise not be suitable for human consumption?

e) One of the leading causes of death in Western society is now related to heart disease and contrasts differently to prior to 1900 when industrial produced seed oils did not exist. Prior to 1900, leading causes of death consisted of infectious diseases (many of which are highly preventable today through medical advancements) such as tuberculosis, measles and pneumonia. Nowadays, animal fats such as lard are no longer widespreadly used as cooking oil and many households and restaurants now use seed oils such canola and soybean oil. If that is the case, is this demonised characterisation of saturated fats found in animal fats be accurate? We also see increased global production and consumption of seed oils since 1911. So what is the cause of this increasing rates of heart disease in modern society if not seed oils?

![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/ad1d4465-abc3-4ccc-a82b-fd5956167fdd)

Although seed oils are classified as vegetable oils but not all vegetable oils are seed oils such as coconut and avocado (they are made from the fruit itself), this analysis considers inclusion of 'vegetable oil' as seed oil. For example, this baby formula product initially lists vegetable oil but in brackets offers the make up of this 'vegetable oil' revealing a blend including sunflower oil which is a seed oil. Often than not, if vegetable oils are used, it would not be uncommon to assume the cheapest form has been used such as canola or soybean.

![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/fc6aaf29-1f7b-476b-927f-0ff2e7be2450)


## DATA
Ingredients information of ~14 000 products were scraped from the Coles Supermarket website. 

**Web Crawl and Scrape**

A crawler program was written in Python to crawl and scrape the Coles website for all food products and ingredients information. The program would crawl through each of the product categories (as set out by COLES), obtain the individual product URLs and then individual product ingredients information scraped. Of note is that the program was interrupted at times and so the program had to be restarted many times. The raw data that was scraped was ultimately split into multiple files.

**Data Cleansing and Formatting**

Before any analysis could take place, some data cleansing and formatting was required.

1) Baby Products consists of both food and non food items. Non food items were filtered out before analysis.
2) The ingredients data were formatted to lower case and the word 'oils' replaced with 'oil' to allow parsing for specific types of seed oil used in the manufacture of the food product.
3) Additional columns were added to indicate presence of specific seed oil types. 1 indicates Yes, 0 indicates No
![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/c3e992ce-bfd4-4f81-9dc3-00f3b9de3265)
4) Final additional column was added to indicated an overall presence of seed oil/s in the product. As long as there was at least 1 indication of 1 value in preceding additional columns, this final column would indicate 1 for Yes.
![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/c1168f68-f462-44e5-8b56-cd5c59d0efcb)![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/e4549483-44a0-4427-a985-d51115b3037a)

5) Some duplicate entries existed e.g. a product might be categorised by Coles as part of 'Drinks' and 'Dairy Eggs Fridge'. The duplicate entries were remove and instead classified as part of only one category. This reduced the total product entries from ~14 000 to ~13 000.

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

Food products sold at Coles were investigated for their presence of seed oils. The food products were split according to these categories (as set out by COLES):
![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/388ba089-369e-49a0-ae0f-0155840028be)

**Total Products examined**: 12834
![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/4de488e9-0b3c-479e-9e5c-307b69309df9)

**Products with Seed oils**: 3906
**% of products with Seed oils**: 30.43%

However when examined products by category, the proportion of products with seed oils painted a different picture for example, 67% of 'Bakery' products had seed oils, 53% of 'Frozen' products had seed oils whilst only 1% of 'Drink' products had seed oils.

![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/bf0baf7d-bfd0-42bc-acae-55c8ca844ae3)

This would make sense since 'Bakery' and 'Frozen' products consist of a lot of processed, pre packaged food items such as microwavable meals and in house made baked items such as cakes and bacon and cheese pizza rolls whilst 'Drink' products often do not require some form of cooking oil to manufacture e.g. soft drinks.
The 'Meat Seafood' and 'Fruit Vegetable' categories were expected to have lower proportion of products with seed oils as the category name suggests only raw products involved. However, both these categories also consisted of prepackaged foods such as preprepared salads with dressing/ sauces with seed oils and processed meat products such as plant based patties and sausages.

Another point of interest is that there were infant formula products at Coles which were manufactured with seed oils such as canola and vegetable oils for the purposes of adding calories to the product. 

**Regarding Specific Forms of Seed Oils Used**

![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/746ccaf1-64bf-444d-acf5-209d8a489ec9)

Majority of products manufactured with seed oils are listed as 'Vegetable Oils' with 'Canola Oil' coming in second with 'Sunflower Oil' coming in third. The bulk of seed oils listed are across these 3. Nearly 50% of the products with seed oils are listed with 'Vegetable Oil' indicates the non desire of food companies to not disclose accurately the type of cooking oil they have used within their products.

![image](https://github.com/TON369777/SEED-OIL-ANALYSIS/assets/156875448/f87a2abb-48a7-462f-8d04-8b1c206e9854)

There was the expectation that a majority of food products at COLES would have seed oils due to the increasing production of seed oils over the years however selecting food products to consume based on proportion of food category would be inaccurate as even food categories of 'Meat Seafood' and 'Fruit Vegetable' also include processed food products containing undesirable ingredients. In that case, concerned consumers should pay attention to the ingredients when selecting food products to consume as even something like baby formula contain seed oils. As expected, raw produce such as meat, fruit and vegetables do not contain seed oils as they are unprocessed food products. Consumers looking to definitively avoid seed oils would do well to consume food products as close as possible to their fundamental form and cook their own food instead of resorting to processed forms of food.
