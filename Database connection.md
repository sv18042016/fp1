---


---

<h1 id="database-connection">Database Connection</h1>
<p>Connection specifies a database connection from which model can retrieve the data.<br>
<strong>1. Click on Database Section</strong>  to setup a database connection.</p>
<p><strong>2.</strong> <strong>Click on +New connection</strong> button to start setting up the connection to database. in general, you specify the below mentioned  fields:<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/demo%20image.png" alt="enter image description here"></p>
<ul>
<li><strong>Name</strong> Specify a name of the connection to define</li>
<li><strong>Database(dialect)</strong> choose a appropriate dialect that matches your <a href="http://connection.at">connection.at</a> present BiPlus  is supporting following list of Database.Further to this we can also include the dialect as per the business requirement.
<ul>
<li>MySQL</li>
<li>Oracle</li>
<li>MS SQL</li>
<li>Vertica</li>
<li>Rest</li>
<li>PSQL</li>
<li>MariaDB</li>
<li>Amazon Aurora(MySQL)</li>
</ul>
<blockquote>
<p>In the most recent release, Bi Plus also supports following list of dialects</p>
</blockquote>
<ul>
<li>Amazon Redshift</li>
<li>Google BigQuery</li>
<li>Snowflake</li>
<li>PostgreSQL</li>
<li>Teradata</li>
<li>Apache Spark</li>
<li>Impala</li>
<li>Amazon Athena</li>
<li>Druid</li>
<li>Cloud Spanner</li>
<li>MemSQL</li>
<li>Hive</li>
</ul>
</li>
</ul>
<blockquote>
<p>Note: In case if your database are not available in the above mentioned list, Bi Plus will include the dialects required.|</p>
</blockquote>
<ul>
<li><strong>Host</strong> Provides the database host path</li>
<li><strong>Database</strong>  identifier name of the database used for connection</li>
<li><strong>Username and Password</strong> to connect the database</li>
<li><strong>Temp database</strong> ( depending on  the selected dialects)  contains a derived set of tables which can be used as per requirement</li>
<li><strong>Maximum connection</strong> maximum number of connection you want to setup</li>
<li><strong>Additional Parameters</strong> include any additional JDBC parameter in this section</li>
<li><strong>Over SSH</strong> protect the data using a user and access key assigned to it</li>
</ul>
<p><strong>3. Dialects</strong> select the accurate dialect from the list using dropdown option.</p>
<p><strong>4. Test Connection</strong> click the button to check if the entered information is running accurately.</p>
<p><strong>5. Add Connection</strong> click the  button to establish and save the connection.</p>
<blockquote>
<p>After establishing the connection you can see the list of connections names on left side toolbar</p>
</blockquote>
<p><strong>6. click on edit</strong> option available on right side of your connection name to make changes.</p>
<p><strong>7. click on delete</strong> option available on far right of your connection name to delete the connection from database.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/screenshot.png" alt="enter image description here"></p>

