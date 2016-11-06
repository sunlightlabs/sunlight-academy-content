<h1>Pivot Tables</h1>

Pivot tables are powerful tools, but it's not always obvious how to use them. Learn how to create and use pivot tables in Excel to aggregate and summarize data that otherwise would require a database.
Welcome to this lesson on using pivot tables. This tool is a terrific way to analyze data in a spreadsheet. It allows you to organize information in a way that otherwise would require a database.

In this module, we'll walk through the process using Excel 2007 for Windows. Other versions of Excel can do the same things, but some of the steps might be slightly different.

So, what is a pivot table, exactly? It's really just a tool for summarizing information. You can use pivot tables to do a number of things with your data, such as counting occurrences of some value, or aggregating data based on common values.

To get started, let's download <a href="http://1.usa.gov/slu5o5">this spreadsheet</a> from data.gov.

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/uploads/datagov.png">

The spreadsheet we're using details U.S. foreign aid since 1946, and it does so by country and by program.

<h3>About the data</h3>

Before we go on, notice the multiple tabs at the bottom of the spreadsheet. The second tab, titled "Economic Historical $," provides monetary figures in real dollars -- that is, how much was actually spent at the time in those years. The third tab, titled "Economic Constant $," provides the data in constant dollars, enabling us to make sensible year-to-comparisons.

Which tab we use will depend on the questions we ask.

Let's say we want to know how much the U.S. spent in 2009 on the various programs across all countries. If we want to understand this figure at today's value (which isn't all that different from 2009), use tab 3. If you want to see it at 2009's values, use tab 2.

<h3>Creating a pivot table</h3>

To create our pivot table, select "Insert" and click "PivotTable." Stay with the default settings in the resulting dialog box and a blank Pivot Table will be placed on a new sheet in Excel.

With our pivot table in place, let's start looking at the data:

<a href="http://www.youtube.com/embed/Okb49d37Uu4?rel=0">Youtube Video</a>



What Excel did was add up all the spending done in all of the countries and organized it by program. So, the U.S. spent about $15.5 million on Child Survival and Health programs around the world in 2009.

Now let's organize this data so we can see where the money is going:

<a href="http://www.youtube.com/embed/Z_Td7XhkzqQ?rel=0">Youtube Video</a>



Of course, it would be a lot easier to read this data if it were formatted properly. No problem:

<a href="http://www.youtube.com/embed/OwkXSBOKcTc?rel=0">Youtube Video</a>



<h3>Working the count</h3>

Another question one might ask this data is, how many foreign aid programs is the U.S. running in each country? This is easily answered using the "count" function.

<a href="http://www.youtube.com/embed/vj63Lazbay0?rel=0">Youtube Video</a>



<h3>Playing the percentages</h3>

Another useful function is calculating percentages. For example, maybe we'd like to break down 2009 program spending by percentage.

<a href="http://www.youtube.com/embed/axOCwmbVEvg?rel=0">Youtube Video</a>



We can also look at what percentage of all aid since 1946 was handed out in 2009. To do this, we'll need to add a new column in our data tab totaling all the years for each country and program. We'll call this column "Total."

<a href="http://www.youtube.com/embed/CN7MF3fgLNo?rel=0">Youtube Video</a>



Now, let's create a new pivot table with "country_name" in the row labels and "Total" in values. Be sure to set total to "sum."

Then we'll need to create a new column in our pivot table:

<a href="http://www.youtube.com/embed/97NJXyeKokw?rel=0">Youtube Video</a>



<h3>Comparisons</h3>

Finally, you can add multiple values if you want to make side-by-side comparisons.

Simply remove "Total" from the value box and instead add two years, say 2000 and 2009. Make sure to set both to "sum of."

<a href="http://www.youtube.com/embed/_RZfRCnMMMM?rel=0">Youtube Video</a>



As you can see, pivot tables are incredibly powerful, if not always intuitive. But, with a little patience, you can start using them to better analyze and understand your data.