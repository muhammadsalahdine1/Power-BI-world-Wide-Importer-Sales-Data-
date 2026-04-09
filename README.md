# Power-BI-world-Wide-Importer-Sales-Data-
## Dataset world_wide_importer_data 
FactSale - DimCity - DimCustomer - DimDate - DimEmployee - DimStockItem


### Let's breakdown the report by questions?


### Quantity of items sold per year ?
create a relationship betweenFactSale's Invoice Date Key and DimDate's Date
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/2.PNG" width="1000">
create bar chart
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/3.PNG" width="1000">

### Let's add some more details to the report. We already found the quantity of items sold per year. 
### Now, I want to know more about the profit made over the years. 
### A card is a great choice because it's simple and adds some elegant interactivity.
- Select the Profit field from FactSale
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/4.PNG" width="1000">

### Select the year 2014 bar. How does the profit card change?
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/5.PNG" width="1000">

### We have the fields Quantity and Profit in our report. 
### It would be interesting to analyze how each Wide World Importers (WWI) salesperson has contributed to the quantity of items sold and the profit generated.
### To do this, we'll add a new dimension table (DimEmployee) and a slicer.
- Create a relationship between FactSale's Salesperson Key and DimEmployee's Employee Key.
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/6.PNG" width="1000">
### Add the Employee field to the slicer.
- Using the slicer you've just added, how much profit did salesperson "Taj Shand" generate for WWI in 2014?
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/7.PNG" width="1000">

