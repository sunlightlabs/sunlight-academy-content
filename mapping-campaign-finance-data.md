<h1>Mapping Campaign Finance Data</h1>

Campaign finance data can be complex and confusing -- for reporters and for readers. But it doesn't have to be. One way to make sense of it all is through mapping. Learn how to turn campaign finance information into beautiful maps, all through free tools. <h3>Getting started</h3>

One of the interesting ways to deal with campaign finance information is to plot it on a map. It can be useful to see where donors to a particular party are located, for example. You can see if donors are concentrated in certain counties. Or, you can aggregate donation amounts and see where most of the money comes from.

To do these visualizations, we need a source for the data and tools for mapping it. That's what this tutorial will guide you through. Specifically, we're going to look at how much Barack Obama raised in various Ohio ZIP code areas for the 2012 election.

We'll start by finding campaign relevant finance information. For that, we'll turn to <a href="http://influenceexplorer.com/">Influence Explorer</a>, and specifically the "Data" tab on the right side of the page.

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/1.jpg" />

Using the data feature of Influence Explorer unlocks the full power of the site by enabling users to query the underlying Influence Explorer databases. For example, we can search for individual contributions from people living in Ohio to Barack Obama during the 2012 election cycle. Here's how we'd do that:

<a href="http://www.youtube.com/embed/1nTWVyZNCAo?rel=0">Youtube Video</a>

Once we download the resulting data, you'll see it's a good bit of data, with more than 1,200 rows and 30 columns.

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/2.jpg" />

<h3>Data clean-up</h3>

To make the rest of the process simpler and faster, it's useful to spend a few minutes cleaning up the data. This spreadsheet contains quite a few columns that aren't relevant to our goals.

In fact, we can remove all BUT the following columns:

<ul>
<li>amount (G)</li>
<li>date (H)</li>
<li>contributor_name (I)</li>
<li>contributor_occupation (L)</li>
<li>contributor_employer (M)</li>
<li>contributor_gender (N)</li>
<li>contributor_address (O)</li>
<li>contributor_city (P)</li>
<li>contributor_state (Q)</li>
<li>contributor_zipcode (R)</li>
</ul>

Even some of those columns we're keeping aren't necessary to the map, but they're useful and interesting nonetheless.

Once we delete the unneeded columns, we'll end up with a spreadsheet that looks like this:

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/3.jpg" />

It's also important to take a moment to familiarize ourselves with the data. If you sort the spreadsheet by the "amount" column, you may notice the existence of negative numbers:

<a href="http://www.youtube.com/embed/zimvgKfWN0I?rel=0">Youtube Video</a>

You might be tempted to remove rows with negative values, but that would be a mistake.

The negative values are listed when campaigns refund donations. This can happen, for example, if the donor was ineligible or had already contributed the maximum.

The next step is to export our spreadsheet as a CSV, or comma separated value document. We need to do this, instead of simply saving it as an Excel spreadsheet, because of the next step. The exact process for exporting as a CSV depends on the version of Excel you're using, but generally you can "save as" or "export" the current file and select "Comma separated values .csv" in the resulting dialog box.

<h3>GeoCommons</h3>

In order to make our data geographically relevant, we're going to enlist the website <a href="http://geocommons.com">GeoCommons</a>. This free service does several important things, including geocoding addresses, creating maps and performing geographic analyses on data.

(Note: If you don't already have a free login for GeoCommons, you'll need to create one.)

Upon logging into GeoCommons, you'll select and upload your CSV file, as shown here:

<a href="http://www.youtube.com/embed/UTYtcFfuaFM?rel=0">Youtube Video</a>

When you upload your file to GeoCommons, you'll be asked to georeference your data. That's a fancy way of saying, "add some geographic information to this file."

You'll get two options. The first is to "join with a boundary dataset," which means you can associate data with area, like states, counties or ZIP code areas. The second option is to "geocode based on an address or place name." As our data includes donor addresses, this second option is what we want to do.

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/4.jpg" />

Now we will see a new page in which we have to tell GeoCommons which fields from our spreadsheet it should use to determine precise locations. This is just a matter of editing the data formats as follows:

<a href="http://www.youtube.com/embed/VapAPPTx6nM?rel=0">Youtube Video</a>

Once you click "Continue," GeoCommons will spend a few minutes analyzing the addresses and setting latitude and longitude coordinates for each row.

Assuming all goes well, you should be presented with a screen that looks like this:

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/5.jpg" />

Next, you'll be asked to "Describe and Share your Dataset." This information is optional, but it's good practice to fill it out as completely as possible.

Once you click "save," you are ready to map and/or analyze the data.

<h3>Analysis</h3>
One of the most powerful and impressive features of GeoCommons is its ability to perform various analyses on the data you uploaded. To get started, click the "analyze" button on the dataset we just uploaded.

You'll then be presented with a bevy of options, from merging datasets to filtering by distance, to performing mathematical functions on the data.

Since our goal is to add up contributions by ZIP code areas, we'll select "aggregation." Then we'll need to select a boundary to aggregate to (ZIP code areas), determine what to do with areas that have no data, and what kind of aggregation we want to do. For example:

<a href="http://www.youtube.com/embed/P-zFNHEPJPs?rel=0">Youtube Video</a>

Once you submit your analysis, GeoCommons will crunch the numbers for a few seconds. The result is a new dataset, so once the analysis is complete, you'll once again be asked to "Describe and Share your Dataset."

<h3>Mapping</h3>
You're now ready to map the data. Although GeoCommons has built-in mapping functions, we're going to take our data to Google and map it there.

The primary reason for this is because Google is much more flexible than GeoCommons regarding how you can design your map.

So, to export our map data, we'll download the KML file from our dataset page.

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/6.jpg" />

This will save a KML file to your computer. A KML file is a form of XML that is specifically formatted for Google's mapping system. (KML stands for Keyhole Markup Language -- Keyhole is the mapping company Google bought and turned into bring Google Maps.)

At this point, we'll turn to Google Docs. Once you log in, click the "Create" button and select "Table." (These are sometimes known as "Fusion Tables," which is what Google initially called them.) You'll then be presented with the option to import a new table. You'll proceed like this:

<a href="http://www.youtube.com/embed/VjcYFpI3WJk?rel=0">Youtube Video</a>

At the end of import process, you'll be presented with your table. We preserved the "Name," "Sum of Amount" and "geometry" columns, as shown here:

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/7.jpg" />

Before we make the map, we need to do a couple of things with this data. First, we should apply a format to the field "sumofamount," which is, after all, a dollar figure. Within the table, go to "Edit" and "Modify columns." You should see a screen like this:

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/8.jpg" />

Now, click on "sumofamount" and change the format to "$1,234.56." That will add a dollar sign and a thousands comma separator to the fields in the column. (Unfortunately, it also adds cents to the values. I say "unfortunately," because our values don't have cents, so it adds an unnecessary ".00" to every number. Oh well.)

Next, let's check to see what the highest and lowest values are for the "sumofamount" column are:

<a href="http://www.youtube.com/embed/6VZFLbmPFBo?rel=0">Youtube Video</a>

It'll be helpful to know these figures later in the process.

Now it's time to make the map. Go to the "Visualize" menu, and select "Map." The resulting screen will plot the ZIP code areas and color them all red. Clicking on one of the red splotches will call up an info box, as you can see here:

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/9.jpg" />

There are still a few things we'd like to do this map. Namely, we want to make the info box a little more meaningful, and we want to color code the areas by the amount donated. That is, we don't want every area to be the same shade of red. Rather, we'd like areas with greater donations to be darker than areas with fewer donations.

Let's start with fixing the info box. Currently it says "Name," followed by the ZIP code, and then "sumofamount," followed by the total donations. The words "Name" and "sumofamount" come from the column headers in our data.

Let's change "Name" to something more meaningful, like "ZIP code area," and "sumofamount" to "Total donated." To make this change, click "Configure info window" and follow along here:

<a href="http://www.youtube.com/embed/0YYDLMUuNSY?rel=0">Youtube Video</a>

We're almost there. Now it's time to color code the map. We'll do that by clicking "Configure styles" and do the following:

<a href="http://www.youtube.com/embed/GA-nVDjf9L4?rel=0">Youtube Video</a>

Once you return to your map, you'll see green splotches all over Ohio. And if you zoom into the Cleveland area, you'll see that's where Obama is raising the most money:

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/10.jpg" />

With our map made, we're ready to publish. We need only to make the map public and get the embed code.

In the upper right, click the "share" button and on the resulting pop-up window, change the access from "Private" to "Public on the web."

<a href="http://www.youtube.com/embed/eiqzgql5W5w?rel=0">Youtube Video</a>

Next, click "Get embeddable link." On the resulting pop-up window, enter your desired width and height and then copy the code beneath the text "Paste HTML to embed in website."

<img src="http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/training/maps/11.jpg" />

Your final step is simply to paste the copied code into your website!

For those who are interested in more advanced ways of manipulating and displaying Fusion Table maps, you can learn more at Google's <a href="https://developers.google.com/fusiontables/docs/sample_code#FTLayers">Maps API page</a>. With the instructions here, you can change the look of the baseman (remove features, colors, etc.), add dropdown menus and more.

You can leave questions and comments in the section below. And if you use these instructions to make a map of your own, please let us know. We'd love to see your work.