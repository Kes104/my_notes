topic: Cloud Computing Applications and Paradigms

### Challenges

1. Security Isolation
2. Performance Isolation
3. Reliability

### Cloud Apps and new ones

Three categories of cloud apps:
- #Processing-pipelines - data-intensive and sometimes compute-intensive applications and represent a fairly large segment of applications currently running on cloud.
- #batch-processing-systems
- #Web-Applications

#Processing-pipelines consist of Batch/Data Processing Systems.
they can be identified as :
1. Indexing - It supports indexing of large datasets created by web crawler engines.
2. Data Mining - It supports searching very large collections of records to locate items of interests.
3. Image Processing - supports image conversion, compress or encrypt images.
4. Video trans-coding - It trans-codes one video format to another. (AVI -> MPEG)
5. Document processing - converts very large docs from one format to another, encrypts the docs or use OCR{Optical Character Recognition} to produce digital-images of docs.

#batch-processing-systems cover a broad range of data-intensive apps in enterprise computing. They need to meet deadlines, Security is critical.
Some of them include :
1. Processing billing and payroll records.
2. Inventory management of large corporations.
3. Automatic testing and verification of software and hardware systems.
4. Generating daily, weekly, monthly and annual activity reports for organisations in retail, manufacturing and other economic sectors.
5. Management of software development.

#Web-Applications they would require scaling up and down by seasonal requirements.

### Architectural styles of CC

*Stateless server* :- those which do not require a client to first establish a connection to the server. Instead, views client request as an independent transaction and responds to it.
*Advantages* 
- client is not affected when server goes down and comes back up between 2 consecutive requests.
- they are simpler, more robust and scalable.

<COBRA> {Common Object Request Broker Architecture}
<SOAP> {Simple Object Access Protocol}
<WSDL> {Web Services Description Language}
<REST> {Representational State Transfer}

### Workflows: Coordination of multiple activities

#workflow-models
#workflow-life-cycle
#workflow-description
#workflow-schema



