---


---

<h1 id="create-project">Create Project</h1>
<p>Select the model section and click projects.</p>
<ol>
<li>click on new project button and specify the below fields:<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model1.png" alt="enter image description here"></li>
</ol>
<ul>
<li>
<p><strong>Project name</strong> enter a project name to identify the model file.</p>
</li>
<li>
<p><strong>Connection</strong> Select the database connection you want to setup from the list provided<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model2.png" alt="enter image description here"></p>
</li>
<li>
<p><strong>Database</strong> Select the database that you want to use for configuration by selecting the checkbox on left side database section as shown below the selected databases are visible on right side of the database section.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model3.png" alt="enter image description here"></p>
</li>
<li>
<p><strong>Tables</strong> select the table fields in the tables section by selecting the checkboxes all the selected tables are visible on the right side of the tables section as shown in the image below,you can also remove the selected tables from database by unchecking the check boxes.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model%204.png" alt="enter image description here"><br>
<strong>2.Auto Build Joins</strong> automatically adapt or take over the join connection which have been enabled in database .<br>
<strong>3.Save project</strong> Click on save button to save the project created.<br>
<strong>4.Click on Edit Button</strong>  to add any additional information to created project then <strong>update</strong> button to save changes.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model5.png" alt="enter image description here"></p>
</li>
</ul>
<h4 id="once-we-save-the-created-project-the-data-is-reflected-in-model-screen-as-shown-in-below-image">Once we save the created project the data is reflected in model screen as shown in below image:</h4>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model7.png" alt="enter image description here"><br>
<strong>Model</strong> defines explore and their relationship with other view. Model is derived using all the below parameters.</p>
<ul>
<li><strong>Project</strong> used for the model</li>
<li><strong>Connection</strong> database connection used for the model.</li>
</ul>
<h4 id="syntax-for-defining-model-parameters">Syntax for defining model parameters:</h4>
<pre><code> {
	"project": "Oracle_test2",
	"info": "Project Info",
	"connections": [
		"Oracle_Build",
}
</code></pre>
<h4 id="parameters-used-in-the-model">Parameters used in the model:</h4>
<ul>
<li><strong>Name</strong> of the database table</li>
<li><strong>Label</strong> labeling the way model should appear in the visualization</li>
<li><strong>Filters</strong> is optional list of filter expression derived for calculation of the measures</li>
<li><strong>Join</strong> establishes the relationship between visualization and views,here we use 3 types of join parameter join,join_type,join_on.
<ul>
<li><strong>Join</strong> can derive the relationship between 2 views based on the condition</li>
<li><strong>Join_type</strong> derives which type of join to apply (Left,Right,inner join)</li>
<li><strong>Join_on</strong> derives the relationship between how to join two tables</li>
</ul>
</li>
</ul>
<h4 id="syntax-for-parameters-defined">Syntax for parameters defined:</h4>
<pre><code>{
			"name": "BI_DELIVERYREPORT",
			"label": "BI_DELIVERYREPORT",
			"filters": [],
			"joins": [
				{
					"join": "BI_CUSTOMERS",
					"join_type": "left",
					"join_on": "${BI_DELIVERYREPORT.CUSTOMERID} = ${BI_CUSTOMERS.CUSTOMERID}"
				}
			]
		},
</code></pre>
<p><strong>5. Click on Save</strong> to save the model.</p>
<blockquote>
<p>Note: you can also edit the created or existing model</p>
</blockquote>
<h4 id="create-a-custom-view">Create a custom view:</h4>
<p>You can create your own set of derived custom table that doesn’t already exist in your database.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model8.png" alt="`"><br>
<strong>6. Click on New Empty view</strong> button to create a derive a new custom view table.<br>
<strong>7. Once the view is created</strong> label the database field and derive the custom table using a SQL query as a result a derived table is created.<br>
Below are the list of parameters used while defining a table :</p>
<ul>
<li><strong>Name</strong> of the custom table derived</li>
<li><strong>label</strong> the custom table</li>
<li><strong>info</strong> provides the description for the table</li>
<li><strong>type</strong> datatype used while deriving a table</li>
<li><strong>database</strong> table used to get the table field</li>
<li><strong>connection</strong> database connection established for creating a new derived table</li>
</ul>
<h4 id="syntax-for-deriving-custom-table">Syntax for deriving custom table:</h4>
<pre class=" language-undefined"><code class="prism language-{ language-undefined">	"name": "CustomView_791",
	"label": "CustomView_791",
	"info": "Description",
	"type": "query",
	"sql": "(SELECT A.STATIONCODE SC,A.ORDERID ORID,A.WHENMADE ORTIME,B.NAME RECEPNAME, A.AMOUNT ORDVAL,A.QUANTITY QTY,A.WAYUSED ORDBY, A.PAYMENTMODE PM,C.NAME CUSTNAME,C.ADDRESS CUSTADDR FROM ROOT.ORDERS A INNER JOIN ROOT.EMPLOYEES B ON A.ORDERATTDID=B.EMPLOYEEID INNER JOIN ROOT.CUSTOMERS C ON A.CUSTOMERID=C.CUSTOMERID)",
	"database": "ROOT",
	"connection": "Oracle_Build",
}
</code></pre>
<h4 id="below-are-the-list-of-function-and--parameters-used-while-defining-a-fields-under-table-">Below are the list of function and  parameters used while defining a fields under table :</h4>
<ul>
<li><strong>name</strong> identifier defined for a field</li>
<li><strong>label</strong>   the derived field</li>
<li><strong>data_type</strong> have supporting parameters and string is used as default parameter while deriving the fields for custom table.below are the list of supporting parameters we use while defining the custom fields,</li>
<li><strong>string</strong> for measures that contain letters or special characters</li>
<li><strong>date</strong> measures that contain dates
<ul>
<li><strong>time_frame</strong> is a derived list of formats from timestamps for instance the following are the available formats hour,day,week,month,quarter, year,date,week_day,date_month,date_quarter, date_hour, year_week.</li>
<li><strong>number</strong> for the measure that contain number</li>
<li><strong>int</strong> for the measure that contains integers</li>
</ul>
</li>
<li><strong>type</strong> can be used as part of dimension or measure</li>
<li><strong>lookup</strong> retrieves a list of values for a specific field either from database using a query or from an item list (it is listed in the filter section during visualization)</li>
<li><strong>operator</strong> is used to retrieve single or multiple values in the filter section while using lookup</li>
<li><strong>SQL</strong> parameter is used define a valid sql expression that results in a field value</li>
<li><strong>summary</strong> is used to retrieve the aggregate field values of the measures using the following options Sum,count,average, maximum,minimum</li>
<li><strong>drill_down_fields</strong> parameter is used to explore the data within the field</li>
<li><strong>show_drill_down _measure</strong> parameter is used to retrieve the data from multiple levels by assigning he true or false condition to the parameter</li>
<li><strong>Visualize</strong> parameter is used as display on-off option of the field in visualization section by assigning true or false condition to the parameter</li>
<li><strong>Number_format</strong> it specifies different set of number formats used for the field values</li>
<li><strong>Currency</strong> is applied to retrieve the values in specified currency applicable</li>
</ul>
<h4 id="syntax-for-defining-fields-in-custom-table">Syntax for defining fields in custom table:</h4>
<pre><code>"fields": [
		{
			"name": "CUSTNAME",
			"label": "CUSTOMER NAME",
			"data_type": "string",
			"type": "dimension",
			"lookup": "",
			"operators": "",
			"sql": "\"CustomView_791\".CUSTNAME",
			"summary": "",
			"drill_down_fields": "SC,ORID",
			"visualise": "true"
]
}
</code></pre>
<p>** 8.Click on save** button to save the custom table view.</p>
<p><img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/model9.png" alt="enter image description here"></p>

