# magmi
magmi bundle fixes

Fixed the magmi bundle product import:
- after magmi import, bundle product does not shown on frontend category page, but detail page can reached via url, 
but options not loaded. 

So this changes fixed this.

But you have to do these steps before import:


Steps:

1) Download 
download and put the modified file to its directory, 
download from there: https://github.com/igi8819/magmi
(plugins/base/itemprocessors/bundle)

2) Modify the import csv file
IMPORTANT:
put these field in .csv file with values:

price_view: 1 (0 = price range, 1= as low as)
price_type: 0 (0 = dynamic, 1 = fixed)
shipment_type: 0 (0 = together, 1 = Separately)
sku_type: 0 (0 = dynamic, 1 = fixed)
weight_type: 0 (0 = dynamic, 1 = fixed)
options_container: container1 ( where product options can be displayed. container1 is higher up the page, near the price. container2 is further down, below the description )
This fields is important in import csv file, so put there!!!!!

After modification put the modified file to the magmi var import directory, where magmi loads import files.

3) Setup magmi
Setup magmi settings (turn in bundle item processor)

4) Do import
Import with magmi (create new one and existing..)

5) Reindex and cache
Reindex all data (before this you have to turn in flat catalog in admin system)
Clear cache

6) Check frontend
Check category page, and product view page.

I put an example csv file. you can download from
https://github.com/igi8819/magmi/tree/master/examples
bundle exmaple file
