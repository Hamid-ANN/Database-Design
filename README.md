# Approaches to processing data

<b>OLTP:</b> 
Online Transaction Processing.  They are application oriented. 
snapshot of data, gigabyte size. This is used by thoudands of people like constumers.
Find a price of a book, costomer transanction, employees hours 


<b>OLAP:</b> 
Online Analytical Processing. Oriented around a certain subject thats under analysis like averahe sale.
OLAP is used in analysts and dada science companies

Olap contains the historical data, archive at the order of terabyte
Calculate books with best profit, Find the averate transction, .. 

<b>Both of them working together. OLTP is stored in an operational database and provide data and clean them for the OLAP warehause. </b>
<b>Before implementing anything we should figure out besinnes requirements</b>






Structuring data:

1. Structured data

Follows a schema
Defined data types & relationships
e.g., SQL,tablesin a relational database



2. Unstructured data

Schemaless
Makes up most of data in the world
e.g., photos, chatlogs, MP3


3. Semi-structured data

Does not follow larger schema
Self-describing structure
e.g.,NoSQL, XML, JSON







# Storing data beyond traditional databases


<b>Traditional databases:</b>

For storing real-time relational structured data ? OLTP

<b>Data warehouses:</b>
For analyzing archived structured data ? OLAP

Organized for reading & aggregating data

Usually read-only

Contains data from multiple sources

Massively Parallel Processing (MPP)

Typically uses a denormalized schema and

dimensional modeling

Data marts

Subset of data warehouses

Dedicated to a specic topic


<b>Data lakes:</b>
For storing data of all structures e.g., raw, operational databases, IoT device logs, real-time, relational and non-relational

Retains all data and can take up petabytes

Schema-on-read as opposed to schema-on-write

Need to catalog data otherwise becomes a data swamp

Run big data analytics using services such as Apache Spark and Hadoop

Useful for deep learning and data discovery because activities require so much data


When we think about where to store the data we should think about how the data get there and in what form:

<b>ETL</b>: Extract trasnform load


<b>ELT</b> Extract  load trasnform



# Database design
- Determines how data is logically stored

How is data going to be read and updated?

Uses database models: high-level specications for database structure

Most popular: relational model

Some other options: NoSQL models, object-oriented model, network model

Uses schemas: blueprint of the database

Defines tables, fields, relationships, indexes, and views



# Beyond the relational model: Dimensional modeling


This is the adaptation of the relational model for data warehouse design. It is optimized for OLAP queries: aggregate data, not updating (OLTP). This is Built using the star schema and Easy to interpret and extend schema.

Two elements of dimensional modeling:
