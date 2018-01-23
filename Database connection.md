---


---

<h1 id="database-connection">Database Connection</h1>
<p>Connection specifies a database connection from which model can retrieve the data.<br>
<strong>1.</strong> <strong>Click on Database Section</strong>  to setup a database connection.<br>
<strong>2.</strong> <strong>Click on +New connection</strong> button to start the Process.<br>
<img src="https://raw.githubusercontent.com/sv18042016/fp1/master/images/demo%20image.png" alt="enter image description here"><br>
Enter the below list of  credential fields.</p>
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
<li>Amazon Aurora(MySQL)<br>
In the most recent release, BiPlus also supports following list of dialects</li>
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
<li><strong>Host</strong>   Provide the database host path<br>
Database  identifier name of the database used for connection<br>
Username and Password  used connect the database<br>
Temp database the database ( depending on  the selected dialects)  contains a derived set of tables which can be used as per requirement<br>
Maximum connection specify the maximum number of connection you want to make<br>
Additional Parameters include any additional JDBC parameter in this section<br>
Over SSH protect the data using a user and accessible key assigned to it</li>
</ul>

