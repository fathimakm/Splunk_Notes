#### Splunk_Notes

# Splunk
1. splunk is a software platform for searching, monitoring, and analyzing machine-generated data.
2. Splunk can ingest data from a variety of sources, including logs, events, and metrics. It then indexes the data and makes it searchable and analyzable through a web-based interface.
3. Splunk users can create custom searches and dashboards to visualize their data and identify trends and patterns.

### Splunk Index
A Splunk index is a logical container for machine-generated data. It is a named collection of events that is stored on disk. Indexes are used to organize and manage data in Splunk.

1. When you create an index, you can specify a number of settings, such as the retention period for the data, the maximum size of the index, and whether the index should be replicated across multiple indexer clusters.
2. Once you have created an index, you can start ingesting data into it. This can be done using a variety of methods, such as forwarders, syslog servers, and the Splunk web UI.
3. Once the data has been ingested, Splunk will parse it and extract key fields, such as the event time, source, and host. This information is used to index the data so that it can be searched and analyzed efficiently.

##### Splunk indexes are used in a variety of ways, including:

1. Searching: Splunk indexes allow you to search through your data quickly and efficiently. You can create custom searches to find specific events or trends.
2. Reporting: Splunk indexes can be used to generate reports on your data. This can help you to track trends, identify problems, and make better decisions.
3. Monitoring: Splunk indexes can be used to monitor your data for changes or unusual activity. This can help you to detect security threats and other problems early on.


Here are some further steps you can take after creating a Splunk index:

- Configure data retention: Decide how long you want to keep the data in the index. Splunk will automatically delete old data after the retention period has expired.
- Configure replication: If you have multiple indexer clusters, you can configure Splunk to replicate the index across them. This will improve the performance of searches and reports.
- Create dashboards: Dashboards allow you to visualize your data and identify trends and patterns. You can create custom dashboards to meet your specific needs.
- Generate alerts: You can configure Splunk to generate alerts when certain events occur in the index. This can help you to detect security threats and other problems early on.



## 3 Roles of Splunk Enterprise
1. Admin : can install apps, ingest data, create knowledge objects for all users
2. power : can create and share knowledge objects with all users of an app and perform real time searches.
3. user : can only see their own knowledge objects

## Roles of Splunk Cloud
1. sc_cloud
2. power
3. user
4. can_delete
5. token_auth
6. apps

- apps available on splunkbase

## notes
### search in splunk
- commands that create statistics and visualization are called transforming commands
- if i search fail* , everything that starts with fail pops up
- boolean operations can be used (NOT, OR, AND)
- boolean operation have an order of evaluation ->  ((NOT, OR, AND), brackets can be used to control the flow of evaluation
- to find exact keyword, place it in " "
- to find keywords with " ", use / to escape `user = " info /" chris/" not in database`

#### commands
1. search terms
2. commands
3. functions
4. arguments
5. clauses

__example__
`index  = network sourcetype= cisco usage = violation |  stats count(usage) as visit`
- index  = network sourcetype= cisco usage = violation -> search term
- | -> pipe
- stats count(usage) as visit -> search component
- stats -> command
- count -> function
- (usage) -> argument
- as -> clause

- we use pipe to tell splunk to send the current results to the next component

- time > index > source > host > sourcetype

  ### Knowledge objects

  Tools that help you and ur users to discover and analyze your data.

  * 5 categories

    1. Data Interpretation
    2. Data classification
    3. Data Enrichment
    4. Data Normalization
    5. Data Models ( aka search time mapping)
   
   * uses
     1. created by one user and can be shared to others, can be saved and reused by multiple people and multiple apps. Also can be used in a search



   
