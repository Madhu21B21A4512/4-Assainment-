# 4-Assainment-Difference between Cassandra and RDBMS
Cassandra: Cassandra is a high-performance and highly scalable distributed NoSQL database management system. Cassandra deals with unstructured data and handles a high volume of incoming data velocity. In Cassandra data is written in many locations also data come from many locations this row represents a unit of replication and the column represents a unit of storage. 

RDBMS: Relational Database Management System (RDBMS) is a Database management system or software that is designed for relational databases and uses Structured Query Language (SQL) for querying and maintaining the database. It deals with structured data and handles moderate incoming data velocity. In RDBMS mainly data is written in one location also data come from one/few locations and a row represents a single record column that represents an attribute. 

Difference between Cassandra and RDBMS:
S.No.	CASSANDRA	RDBMS
1.	Cassandra is a high performance and highly scalable distributed NoSQL database management system.	RDBMS is a Database management system or software which is designed for relational databases.
2.	Cassandra is a NoSQL database.	RDBMS uses SQL for querying and maintaining the database.
3.	It deals with unstructured data.	It deals with structured data.
4.	It has a flexible schema.	It has fixed schema.
5.	Cassandra has peer-to-peer architecture with no single point of failure.	RDBMS has master-slave core architecture means a single point of failure.
6.	Cassandra handles high volume incoming data velocity.	RDBMS handles moderate incoming data velocity.
7.	In RDBMS there is limited data source means data come from many locations.	In Cassandra there are various data source means data come from one/few location.
8.	It supports simple transactions.	It supports complex and nested transactions.
9.	In Cassandra the outermost container is Keyspace.	In RDBMS the outermost container is database.
10.	Cassandra follows decentralized deployments.	RDBMS follows centralized deployments.
11.	In Cassandra data written in many locations.	In RDBMS mainly data are written in one location.
12.	In Cassandra row represents a unit of replication.	In RDBMS row represents a single record.
13.	In Cassandra column represents a unit of storage.	In RDBMS column represents an attribute.
14.	In Cassandra, relationships are represented using collections.	In RDBMS relationships are represented using keys.

cqlsh is a command-line interface for interacting with Cassandra using CQL (the Cassandra Query Language). It is shipped with every Cassandra package, and can be found in the bin/ directory alongside the cassandra executable. cqlsh is implemented with the Python native protocol driver, and connects to the single specified node.

Compatibility

cqlsh is compatible with Python 2.7.

In general, a given version of cqlsh is only guaranteed to work with the version of Cassandra that it was released with. In some cases, cqlsh may work with older or newer versions of Cassandra, but this is not officially supported.

Optional Dependencies

cqlsh ships with all essential dependencies. However, there are some optional dependencies that can be installed to improve the capabilities of cqlsh.

pytz

By default, cqlsh displays all timestamps with a UTC timezone. To support display of timestamps with another timezone, install the pytz library. See the timezone option in cqlshrc for specifying a timezone to use.

cython

The performance of cqlsh’s COPY operations can be improved by installing cython. This will compile the python modules that are central to the performance of COPY.

cqlshrc

The cqlshrc file holds configuration options for cqlsh. By default, the file is locagted the user’s home directory at ~/.cassandra/cqlsh, but a custom location can be specified with the --cqlshrc option.

Example config values and documentation can be found in the conf/cqlshrc.sample file of a tarball installation. You can also view the latest version of the cqlshrc file online.

cql history

All CQL commands you execute are written to a history file. By default, CQL history will be written to ~/.cassandra/cql_history. You can change this default by setting the environment variable CQL_HISTORY like ~/some/other/path/to/cqlsh_history where cqlsh_history is a file. All parent directories to history file will be created if they do not exist. If you do not want to persist history, you can do so by setting CQL_HISTORY to /dev/null. This feature is supported from Cassandra 4.1.

Cassandra Cluster

In this Cassandra tutorial, we will go through one of the main parts of the Cassandra database i.e. Cassandra Cluster. Moreover, we will see the meaning of Cluster and different layers in Cluster. This article will guide through the parts of the cluster and the builders associated with it.

So, let’s start Cassandra Cluster.

The cluster is a collection of nodes that represents a single system. A cluster in Cassandra is one of the shells in the whole Cassandra database. Many Cassandra Clusters combine together to form the database in Cassandra.

A Cluster is basically the outermost shell or storage unit in a database. The Cassandra Cluster contains many different layers of storage units. Each layer contains the other.
Let’s Explore Cassandra Applications
The following are different layers in a Cassandra Cluster:
Node Cluster

Node is the second layer in a cluster. This layer basically comprises of systems or computers or storage units. Each cluster may contain many nodes or systems. These systems or nodes are connected together.

They collectively share data through the replication in Cassandra and independently as well. The replication factor in the nodes allows the user to have a redundancy for the data stored.

Keyspace

The keyspace is the next layer of the storage. In a node, there are many keyspaces. These keyspaces are basically the outermost storage unit in a system. They contain the main data. The data distributed according to their properties or areas.
Let’s revise Cassandra API

c. Column Families

The next layer is the column families. The keyspace is further divided into column families. These column families have different areas or headings under which the data is distributed. In a keyspace, these column families are categorized into different headings or titles.

These titles further contain different layers of storage units. These column families can also be characterized by tables. The column families differ from the tables through their APIs.

d. Rows

The next layer in the database is of the Rows as according to column families. The Rows are basically the classification under which the column family is divided. These classifications, in turn, create specific distribution criteria for the entries.   
Let’s discuss Cassandra Architecture.

e. Column

This is the innermost layer in a database. The column basically is divided into different titles or headings. These headings contain the main data regarding the specific entry.

3. Cluster Builder

The cluster is the main entrance for the data into the database. The driver of this belongs to com.datastax.driver.core package. Using a set of commands user can initiate the Cluster Builder. This allows the user to perform various detailed operations while building a cluster.

The Cassandra Cluster Builder is basically an interface that holds connections to the clusters. This is also helpful to execute CQL queries and statements.

Different commands and methods are used to perform various operations in Cassandra Cluster Builder.

Have a look at Cassandra Data Types

Session connect(): It allows the user to create a new session on the cluster. Apart from this it initializes the new session.void close(): It allows the user to close the cluster session instance.static Cluster.Builder builder(): It allows the user to create a new Cluster.Builder instance.Cluster.Builder addContactPoint(): This allows the user to add a contact point a cluster.Cluster build(): This command allows the user to build a cluster with the given or default contact points.ResultSet execute(): This allows the user to execute a query. The query may contain a statement object or it may be a string object.PreparedStatement prepare(): This allows the user to prepare a provided query. This query can be provided either in the form of a statement or a string.

Read Data Definition Command – Cassandra Query Language
So, this was all about Cassandra Clustering. 

Classes are interrelated to each other in specific ways. In particular, relationships in class diagrams include different types of logical connections. The following are such types of logical connections that are possible in UML:

AssociationDirected AssociationReflexive AssociationMultiplicityAggregationCompositionInheritance/GeneralizationRealization" i-amphtml-auto-lightbox-visited="" style="max-width: 100%; display: block !important;">Relationships in UML class diagramsAssociation

" i-amphtml-auto-lightbox-visited="" style="max-width: 100%; display: block !important;">Association

is a broad term that encompasses just about any logical connection or relationship between classes. For example, passenger and airline may be linked as above.
Reflexive Association

" i-amphtml-auto-lightbox-visited="" style="max-width: 100%; display: block !important;">Reflexive Association

This occurs when a class may have multiple functions or responsibilities. For example, a staff member working in an airport may be a pilot, aviation engineer, a ticket dispatcher, a guard, or a maintenance crew member. If the maintenance crew member is managed by the aviation engineer there could be a managed by relationship in two instances of the same class.

Multiplicity

" i-amphtml-auto-lightbox-visited="" style="max-width: 100%; display: block !important;">Multiplicity

is the active logical association when the cardinality of a class in relation to another is being depicted. For example, one fleet may include multiple airplanes, while one commercial airplane may contain zero to many passengers. The notation 0..* in the diagram means “zero to many”.

Aggregation

" i-amphtml-auto-lightbox-visited="" style="max-width: 100%; display: block !important;">Aggregation

refers to the formation of a particular class as a result of one class being aggregated or built as a collection. For example, the class “library” is made up of one or more books, among other materials. In aggregation, the contained classes are not strongly dependent on the lifecycle of the container. In the same example, books will remain so even when the library is dissolved. To show aggregation in a diagram, draw a line from the parent class to the child class with a diamond shape near the parent class.

To show aggregation in a diagram, draw a line from the parent class to the child class with a diamond shape near the parent class.
Composition

" i-amphtml-auto-lightbox-visited="" style="max-width: 100%; display: block !important;">Composition

The composition relationship is very similar to the aggregation relationship. with the only difference being its key purpose of emphasizing the dependence of the contained class to the life cycle of the container class. That is, the contained class will be obliterated when the container class is destroyed. For example, a shoulder bag’s side pocket will also cease to exist once the shoulder bag is destroyed.

To show a composition relationship in a UML diagram, use a directional line connecting the two classes, with a filled diamond shape adjacent to the container class and the directional arrow to the contained class.

Inheritance / Generalization

" i-amphtml-auto-lightbox-visited="" style="max-width: 100%; display: block !important;">Inheritance

refers to a type of relationship wherein one associated class is a child of another by virtue of assuming the same functionalities of the parent class. In other words, the child class is a specific type of the parent class. To show inheritance in a UML diagram, a solid line from the child class to the parent class is drawn using an unfilled arrowhead.

Realization

" i-amphtml-auto-lightbox-visited="" style="max-width: 100%; display: block !important;">Realization

denotes the implementation of the functionality defined in one class by another class. To show the relationship in UML, a broken line with an unfilled solid arrowhead is drawn from the class that defines the functionality of the class that implements the function. In the example, the printing preferences that are set using the printer setup interface are being implemented by the printer.


. In general, an object refers to any item, either in the physical or virtual world. For example, a computer is considered an object in the physical world. In the virtual world, a document, file, folder, icon, picture are all considered objects.

2. In computer graphics, an object refers to an item within a graphic, such as a graphic circle or a square.

3. When dealing with computer programming and data objects, see the object-oriented programming definition.

4. When referring to HTML, the <object> tag is used to designate an object embedded into a web page.

Nesting, OBJ, Object-oriented programming, Programming terms, Software terms









