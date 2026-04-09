<img width="1862" height="727" alt="image" src="https://github.com/user-attachments/assets/5eff2ca7-9205-4866-bf7a-a70ffb2c818c" /># Power-BI-world-Wide-Importer-Sales-Data-
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
- Using the slicer I've just added, how much profit did salesperson generate for WWI in specific year?
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/7.PNG" width="1000">


### Wide World Importers sells two types of products: chilled and dry. 
### This is recorded in the database because chilled products require a different kind of packaging. 
### To compare these product types, I will add the quantity of products sold that are chilled or dry to the column chart.
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/8.PNG" width="1000">

### Add a table to our report with the details of sales transactions. 
### With the interactivity of Power BI, this will allow us to see examples of sales based on our selection.
- Add the dimension field Employee to the table.
- Add the fact fields to the table: Description, Quantity, Total Including Tax, Profit.
- Using the table's total row,we can answer question like: how much "Total Including Tax" did "Sophia Hinton" generate in 2016?
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/9.PNG" width="1000">


### Raw data usually doesn't arrive in the perfect form when you account for human errors, bugs, and file conversion. 
### Power BI accounts for this with the Power Query Editor, which allows us to transform data before loading it. 
### Here, I will load another dimension called DimCustomer, except unlike the others, this file will need to be edited prior to loading.
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/10.PNG" width="1000">

### Remove the first row. It contains mostly blanks and does not provide any useful information.
- To remove the first row, select the Remove Rows button on the top Home menu.
- Select Remove Top Rows and specify 1 row in the input, since we only want to remove that one row.
### Make the resulting first row the header row.
- Select Use First Row as Headers from the top Home menu.
### Delete the columns Valid From and Valid To.
- While selecting the columns you would like to remove, select the Remove Columns button in the top Home menu.
### Close and apply.
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/11.PNG" width="1000">


### FactSale and DimCustomer should be connected by Customer Key.
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/12.PNG" width="1000">

### Make a clustered column chart using Buying Group from DimCustomer and Total Including Tax from FactSale.
### Change it so that the value is the minimum of Total Including Tax.
### According to total including tax, how much was the cheapest sale made to Tailspin Toys?
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/13.PNG" width="1000">

### Earlier you practiced cleaning data at row-level, like deleting erroneous rows or changing the header row. 
### Now, we'll take a look at issues at the column-level.
### Create a Card visualization with the Credit Limit field from DimCustomer.


### The card show ? -, which is unexpected! Edit the query of DimCustomer to open up the Power Query Editor and fix the Credit Limit column.
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/14.PNG" width="1000">

### Edit the query of DimCustomer to open up the Power Query Editor and fix the Credit Limit column.
- Replace values so that ?s are replaced with blanks in Credit Limit.
- Repeat so that -s are replaced with blanks for the Credit Limit column.
- Find the Replace values button in the top menu to the right of the Group By button. 
- The first value inputted should be either ? or - and the second value should be blank.
- Change the data type of Credit Limit from Text to Decimal Number.
- Close and apply and return to the Report view. In the card, change the value to be the average Credit Limit.
<div>
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/15.PNG" width="500">
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/16.PNG" width="500">
</div>

### Let's improve the formatting of the Profit and the Total Including Tax columns so it's immediately clear they are monetary values, unlike Quantity.
- In the Table view of FactSale, select the Total Including Tax column.
- Using Column tools, change the format to Currency.
- Change the number of decimal places shown to 2 instead of Auto.
- Change the default aggregation from Sum to Average .
- Repeat the same format and decimal place changes to the Profit column.
 <img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/17.PNG" width="500">

### Making maps with geographic data
#### Maps are an engaging way to present data with a geographic layer. 
#### Imagine we wanted to depict the profit each state in the US generates. 
#### We could create a bar chart showing the states and the profit they generate. However, since there are 50 states, 
#### a map is much easier to scan for patterns and outliers.
#### Load the dimension table DimCity.
#### make sure a relationship is found between DimCity and FactSale.
#### In the Table view, change the Data category of DimCity's State Province to "State or Province".
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/18.PNG" width="500">

### In the Table view, change the Data category of DimCity's State Province to "State or Province".
### Make sure the default summarization for Profit from FactSale is "Average".
### Create a Map visualization using State Province as Location and Profit as Bubble size.
### Add a Slicer for the Buying Group field from the DimCustomer table.
### We can ask quuestions like: Using the map and the slicer, which state generates the highest average profit for the "Wingtip Toys"?
<img src="https://github.com/muhammadsalahdine1/Power-BI-world-Wide-Importer-Sales-Data-/blob/main/19.PNG" width="500">
