<H1>Power BI Notes</H1>
<p>In this repo I will cover Power BI concepts which will include functions of Power Query, DAX Queries, Graphs, Charts, UI/UX, way of presentation and more.</p>

<H2>Power Query</H2>
<p>Power Query is a data connection and transformation tool in Power BI, Excel, and other Microsoft products that allows users to extract, transform, and load (ETL) data from various sources. 
It provides a user-friendly, no-code interface for cleaning and reshaping data before loading it into a data model.</p>

<h4>Key Features</h4>
<ul>
  <li><p><b>Data Connectivity:</b> Connects to multiple data sources (Excel, SQL, APIs, etc).</p></li>
  <li><p><b>Data Transformation:</b> Cleans and reshapes data (removing duplicates, merging tables, etc).</p></li>
  <li><p>Updates data automatically when sources change.</p></li>
  <li><p>M Language (M Code):</b> Uses a formula language for advanced data transformation.</p></li>
</ul>

<H2>Data Connectors / Data Extraction</H2>

<p>You can connect your data along with IBM server, Python, BigQuery, etc.
Here are some common examples</p>

<img src="images/dataConnector.png" alt="data connector">

<p>You can extract any datasets in power query using get data options, following it browsing your datasets from your respective folders.</p>

<img src="images/dataFolder.png" alt="data folder">
<img src="images/folderPath.png" alt="folder path">
<img src="images/pizzaSales.png" alt="pizzaSales">

<p>After which you will get the preview of your datasets and you need to click on transform data.</p>
<p>Once you will click on transform data, Power Query Editor will open in which you can transform your data and find hidden insights from your data.</p>

<img src="images/transformData.png" alt="transform data">

<p>Now right click on Binary and select 'Add as New Query' in order to rename your dataset name.</p>

<img src="images/binary.png" alt="binary">

<p>After this procedure you need to click on data file name.</p>

<img src="images/order.png" alt="order">

<p>Now you can change the file name so that you can recognise your multiple data files name.</p>

<img src="images/fileName.png" alt="file name">

<p>Similarly change all the data files names for proper format.</p>

<img src="images/allFiles.png" alt="all file">

<h2>Basic Transformations</h2>

<h3>Setting Column</h3>

<p>Now, as checked in pizza types data file, column names were wrongly set, thus we can change it by using (Use First Row as Headers) in Transform page.</p>

<img src="images/wrong_columns.png" alt="wrong column">
<img src="images/correct_columns.png" alt="correct column">

<h3>Dates</h3>

<p>If suppose you want to extract month from the dates, you need to:
<ul>
<li>Add new column, you don't have to edit existing column</li>
<li>After that, click on Dates column and then select dates</li>
<li>And then you can select month and then name of the month in order to extract month.</li>
<li>After which you can notice we have extracted name of the month in new column.</li></p>

<img src="images/date1.png" alt="date">
<img src="images/date2.png" alt="date">

<h2>Text Tools</h2>
<h3>Merging two columns</h3>
<p>If you want to merge any two columns then you have to select two colums, and after selecting it you need to select merge option from transform.</p>

<img src="images/merge1.png" alt="merge">

<p>Once you have select merge, make sure you select space as seperator, or vice a versa.
After which you can see a column has been generated as merged, you just need to rename it according to your condition. I have renamed here it as Full Name.</p>

<img src="images/merge2.png" alt="merge">

<h3>Extraction</h3>
<p>Suppose we want to extract a username from email id in new column<p>

<p>First we will click on extract button and then we will select text before delimeter which we will take as @, since we want to extract username from email id, but suppose you want to extract domain from email id, then you must select text after delimeter.<p>

<img src="images/extract1.png" alt="extract">
<img src="images/extract2.png" alt="extract">
<img src="images/extract3.png" alt="extract">
<img src="images/extract4.png" alt="extract">

<h3>Removal of Null and Duplicate Values</h3>

<p>For removal of null values there is option on tool bar which is replace values in which you call replace NULL as null which will show NULL values and it will be easy to remove them.

<img src="images/null1.png" alt="null">
<img src="images/null2.png" alt="null">

<p>After which we can we can fill all these null values using fill down or fill up.

<img src="images/null3.png" alt="null">

<p> And now you can see null values has been removed from data.</p>

<img src="images/null4.png" alt="null">

<h3>Removal of Duplicate Values</h3>

<p>There is a option of removing duplicates in your row option when you right click on column name you wwill get option as Remove Duplicates which will help in removing duplicates from your rows</p>

<img src="images/duplicate1.png" alt="duplicate">

<h2>Numeric Tools Using PowerQuery</h2>

<p>If we want to find any statistical values such as average, maximum or minimum we can use statistics given in option, but it will be better to use DAX queries in terms of finding statistical values.</p>

<img src="images/num1.png" alt="numeric">

<p>Q1: Find the total sales from the table order details</p>

<p>Ans: First we will add a new column i.e. add custom column, after which we will select two columns, first column which contains the number of product ordered, i.e. quantityOrdered and second we will select the column which contains price of each product, i.e. priceEach.</p>

<p>And After selection apply multiplication between both the columns in order to find the total sales.</p>

<img src="images/num2.png" alt="numeric">

<p>There are several other Mathematical functions such as Scientific calculations like Logarithmic, Exponential etc calculations, Trignometric calculations, Round up or Round down calculations, etc. You can explore each one to find out hidden insights from your data.</p>

<h2>Date and Time</h2>

<p>When anyone make orders, date and time are always recorded, and based on date and time we can find out insights, that on which month product was ordered mostly, on which month company had more profits, we can find hidden trends, which can help your business to grow in near future.</p>

<p>Q2: How can we remove NULL values from date and time column?</p>

<p>Ans: First change date column type in string format instead of date.</p>

<img src="images/dates1.png" alt="dateTime">

<p> Now you will be able to see NULL values, which you have to replace as 0 instead of null. It will start giving you error, but you need to remove your error rows as given in the picture.</p>

<img src="images/dates2.png" alt="dateTime">

<p> Change the type again in Date format after which it will start giving error</p>

<img src="images/dates3.png" alt="dateTime">
<img src="images/dates4.png" alt="dateTime">

<p>Now select remove error rows in order to remove error from that particular column after which your null values will be removed from Date column.<p>

<img src="images/dates5.png" alt="dateTime">

<p>Q3: Extract the order month from the data</p>

<p>Ans: In order to extract month from orderDate column, we will select add column in task bar, and select date from tool bar, after which we can select name of the month, and extract it.</p>

<img src="images/dates6.png" alt="dateTime">
<img src="images/dates7.png" alt="dateTime">

<p> Similarly we can select week and year</p>