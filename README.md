https://coderacademy.instructure.com/courses/288/assignments/1464

```
Q1.	Describe the architecture of a typical Rails application (200-300)
```

![rails mvc](/docs/mvcrails.png)

At a high level the typical Rails application will be coded under two guiding principles, DRY - Don't Repeat yourself, e.g don't duplicate code and "Convention over Configuration" which means rails has certain conventions that it wants you to use when developing in rails. e.g naming conventions such as matching names and capitalization.

The typical architecture of a Rails application relies on a framework known as the Model-View-Controller or MVC. It splits the functionality of the rails application into three distinct parts, the model, the view and the controller.

The Model (also known as active record) primarily deals with data and the manipulation of the database. The model also makes use of Object Relational Mapping to manipulate data which allows us to interact with the database without having to write SQL plus we get the added benefit of being able to switch databases e.g postgresql, mysql etc.
The View (action view in rails) handles user interfaces and graphical components that the user will see.
And lastly the Controller (action controller) interacts with both the model and views. The Controller handles incoming requests from users/browsers and also acts as a middle-man to direct requests from the view to the model and vice-versa. Your standard application may make use of many different models, views and controllers.

The typical rails application uses puma as webserver and relies on routes that are defined in routes.rb to direct http requests to the correct controller and action. It can be run locally on localhost:3000 or deployed on services such as heroku.

The rails application may also have styling derived from the Asset Pipeline, the pipeline is a framework that allows rails to link assets and styling files together to allow for faster processing.

#### References

- https://www.tutorialspoint.com/mvc_framework/mvc_framework_introduction.htm
- https://guides.rubyonrails.org/getting_started.html#what-is-rails-questionmark
- https://guides.rubyonrails.org/routing.html
- https://blog.bitsrc.io/what-is-an-orm-and-why-you-should-use-it-b2b6f75f5e2a
- image - https://betterexplained.com/articles/intermediate-rails-understanding-models-views-and-controllers/

---

```
Q2.	Identify a database management system (DBMS) commonly used in web applications (including Rails) and discuss the pros and cons of this database (150-250)
```

Postgresql is a database management system that is commonly used in web applications. It is supported by Heroku and recommended as the default for Rails applications. Postgresql is defined as an open-source object relational database management system, it makes use of SQL and also has additional features that extend the language.

I've compared Postgresql to MySQL in the following paragraphs, to aid in demonstrating the pros and cons of Postgresql.
Postgresql makes use of an object relational database which is useful for features such as table inheritance that are missing from other database management systems such as MySQL. The pros of Postgresql include it being highly extensible, supports wide range of data types, and also handles concurrency better than MySQL.

The cons of Postgresql include lower popularity than other databases such as Oracle and MySQL, this could lead to issues such as limited documentation, lack of tools and support. In an article by Uber, they talk about moving from Postgres to MySQL due to issues they had with difficulty upgrading to newer releases of Postgres, inefficient data replication, inefficient data writing and issues with table corruption- this was due to a bug in one of the newer releases.

#### References

- https://www.postgresqltutorial.com/what-is-postgresql/
- https://www.postgresql.org/about/\
- https://www.keycdn.com/blog/popular-databases
- https://developer.okta.com/blog/2019/07/19/mysql-vs-postgres
- https://db-engines.com/en/ranking
- https://eng.uber.com/postgres-to-mysql-migration/

---

```
Q3. Discuss the implementation of Agile project management methodology (200-300)
```

The Agile methodology was developed with the goal of improving software development. Agile's four main values are an emphasis
on

- Valuing individuals and interactions over processes and tools
- Developing working software versus documentation
- Collaborating with customers versus contract negotiation
- Quickly responding to change versus following a plan

The Agile methodology advocates developing projects and software through constant iteration and collaboration to address the needs of customers.

It may be useful to compare the Agile and Waterfall methodology as they're both used in project management but under different circumstances.

In the past software was mainly developed through the waterfall methodology, at the time it was a useful way to develop software as requirements and technology were slow in changing. It was also easy to understand and follow, as each phase had clear goals. Customers were only involved at the start and end of a project. This, however, could lead to issues such as customer's needs changing over the software development period, this was usually expensive to address due to rewriting/scrapping of projects and code.

In contrast, in Agile, customers are constantly involved throughout the development of the project and their feedback can be quickly incorporated into the project. Agile also relies on short sprints or cycles that involve designing, building, testing and review. These cycles can repeat and this is in contrast to the waterfall method which generally has longer time periods and non-repeating phases.

<br>
Below is an example of a 3 cycles or sprints linking together.

![agile loop](docs/loop.png)

<br>

In today's age with the rapid development of start-ups and software, organisations have to be flexible and quick to respond to customer's needs. The agile method caters to this need by allowing for rapid prototyping and development of software, this allows customers to examine the progress of software development quickly, in contrast to the waterfall methodology, in which, projects may take years before they have a product to show.

#### References

- https://www.agilealliance.org/agile101/12-principles-behind-the-agile-manifesto/
- https://www.infoworld.com/article/3237508/what-is-agile-methodology-modern-software-development-explained.html
- https://www.guru99.com/waterfall-vs-agile.html
- https://www.projectmanager.com/software/use-cases/waterfall-methodology
- image - https://www.mendix.com/blog/agile-process-why-you-need-feedback-loops-both-during-and-after-sprints/

---

```
Q4.	Provide an overview and description of a standard source control workflow (100-200)
```

A standard source control workflow would be implemented through the use of a version control system such as Git. Git helps to keep track of changes made to code, this is done through pushing snapshots of the current source code to an online or remote location known as a repository. Git has extensive logs of changes made to code which allows for powerful version control.
In the typical project there will be one main source code known as the master branch which is not, typically, directly used when writing code.
New features are typically developed in branches, developers can make use of branches which allow you to make a copy of the master code and edit it without affecting the original, this can ensure that the master branch always has working code. When the feature or code is completed on a branch it can be tested and merged back with the master code, this would usually be done through a pull request which is essentially asking permission to merge the branch code with the master, the pull request also gives other developers a chance to review the code and suggest changes.

#### References

- https://www.howtogeek.com/180167/htg-explains-what-is-github-and-what-do-geeks-use-it-for/
- https://www.atlassian.com/git/tutorials/why-git

---

```
Q5.	Provide an overview and description of a standard software testing process (e.g. manual testing) (100-200)
```

A standard software testing process could be the use of automated testing, this testing involves the use of automation software to carry out the job of testing.
The process of automated testing would closely follow the software testing life cycle (STLC). It begins with gathering requirements which defines what should be tested, a feasibility analysis - to see if automation is possible/within budget, a requirement traceability matrix - which would detail test scenarios and their status(whether they pass/fail).
A testing plan can then be made which will detail the criteria and strategy for the automation test, it may detail what automation software to be used, costs involved, training required and what automation testing framework may be used.
Test case development and execution will involve the creation of automation scripts for each test case and the running of those automation tests. Detailed logs and reports will be collected regarding each case.
The test cycle closure is the final stage and will be an evaluation of the overall cycle and metrics obtained from testing. This may involve analysis of test findings and list strategies to be incorporated into future testing cycles.

#### References

- https://www.guru99.com/automation-testing.html
- https://www.guru99.com/software-testing-life-cycle.html#2
- https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing
- https://www.guru99.com/traceability-matrix.html

---

```
Q6.	Discuss and analyse requirements related to information system security and how they relate to the project (100-200)
```

In regards to information system security requirements there are 3 major aspects that are regarded as important. They are:

- Confidentiality - who has access to information, confidentiality deals with authorization and generally keeping information safe
- Integrity - making sure data isn't corrupted, data is specific enough, and only changed with authorization
- Availability - making sure that authorized users have prompt access and services are available. Can be important in regards to critical services such as air traffic control and many businesses that operate online.

There are also other requirements such as business, regulatory and customer obligations that we must meet. Depending on the project that is being built we need to analyse to what degree, do we enforce each of our requirements and obligations. E.g for a health service app we may need stricter record-keeping and strict authorization on access to records to comply with The Privacy Act. 

The best option would be to systematically analyse our requirements starting with the regulatory obligations and move down the chain of concern. It may also be useful to produce a framework or report on our infosec requirements. 

Below is an example of requirements that we could base a report on

![infosec framework](docs/infosec.PNG)

#### References

- https://www.techopedia.com/definition/24840/information-systems-security-infosec
- https://www.nap.edu/read/1581/chapter/4
- https://www.proserveit.com/blog/information-security-requirements
- image - https://www.protectivesecurity.gov.au/information/Pages/default.aspx

---

```
Q7. Discuss common methods of protecting information and data and how you would apply them to the project (100-200)
```

A common method of protecting information and data would be to implement authentication, this could be done through the use of a gem such as Devise to require users to have a login and password before they could access the application. A benefit of authentication is this would protect personal user data and information in a quick and simple way. Cons of using a user login system, is that it's up to users to be vigilant with their passwords and to also generate complex and unique passwords.

We could also implement authorization as a method to protect data, this would restrict the permissions of users. For example we would only want users to be able to change their contact details and not someone elses. This also ties into the principle of giving entities the fewest privileges possible. For example an admin may have the power to remove a user but we would disable that function for anyone who wouldn't require it, e.g other users or even an employee. This reduces our risk to vulnerabilities because if you gave that permission to users or employees who didn't require it, they also become points of failure.

#### References

- https://www.keycdn.com/blog/web-application-security-best-practices
- https://www.synopsys.com/blogs/software-security/complete-web-application-security-testing-checklist/

---

```
Q8.	Research what your legal obligations are in relation to handling user data and how they can be met for the project (100-200)
```

The Office of the Australian Information Commissioner (OIAC) provides a set of guidelines known as The Australian Privacy Principles (APP), the APP lists 13 principles that help protect the privacy of an individual. With these guidelines as a reference we can construct a general idea of how we should be handling user data.

<br>
Displayed below is a summary of the Australian Privacy Principles

![app 13 principles](/docs/app13.png)
<br>
<br>
Before we even write any code we can outline how we will handle user data, what data will be collected, how we will notify/inform users about what data we have of them and what security measures we can implement.

To meet our legal and moral obligations to users to protect their data,
we can employ authorization through limiting of user access, so that entities only have access to their own data and authentication through login/password and multifactor-authentication, so that entities logging in are who they claim to be.

We can also implement anonymisation of data and make it harder to read/decrypt by using password hashing. Even simple policies such as requiring users to implement complex passwords can help us protect user data.

Lastly, we can also consult with cybersecurity companies to have them assist us in meeting our legal obligations. They can also inform us on how data should be handled and perform penetration tests on our systems for vulnerabilities.

#### References

- https://www.oaic.gov.au/privacy/guidance-and-advice/data-breach-preparation-and-response/part-1-data-breaches-and-the-australian-privacy-act/
- https://www.oaic.gov.au/privacy/australian-privacy-principles-guidelines/
- https://auth0.com/blog/hashing-passwords-one-way-road-to-security/
- image - https://www.oaic.gov.au/assets/privacy/guidance-and-advice/app-quick-reference-tool.pdf

---

```
Q9.	Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure. (100-200)
```

A relational database model organizes it's database into a collection of relations or tables. It should be noted that this doesn't affect the physical storage of data. A table consists of rows and columns, each row (also known as a tuple) in a table signifies a unique record within the table and represents related data, each row will also have a column called a primary key that uniquely identifies it, while the other columns in a table will list attributes of the data being modeled. Relations between different tables can be encoded through the use of foreign keys, which are primary keys that sit in other tables.

It should also be noted that sometimes a combination of two or more columns can be used as a primary key and this is known as a composite key.
More specifically, regarding data stored in columns, the data is typically of one data type, e.g for a "dollar amount" column that stores integers,should not have strings in it.

<br>

Below is an image of a typical relation/table

![relational db](docs/q9db.png)

#### References

- https://www.oracle.com/database/what-is-a-relational-database/
- https://databasemanagement.fandom.com/wiki/Relational_Database_Model
- https://opentextbc.ca/dbdesign01/chapter/chapter-7-the-relational-data-model/
- image - https://www.guru99.com/relational-data-model-dbms.html
- https://www.techopedia.com/definition/6572/composite-key

---

```
Q10.	Describe the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database. (100-200)
```

There are 3 typical types of data integrity that we can talk about when trying to enforce data integrity upon a relational database. These types are:

- Entity Integrity (also known as key constraints) - this involves the use of primary keys to uniquely define records within a database e.g primary key can't be null
- Referential Integrity - this refers to the validity of foreign keys and whether they point to valid tables or should be null
- Domain Integrity - this refers to columns being within the defined domain, e.g an "age" column shouldn't have negative numbers

With these integrity constraints in mind, we can enforce these in a relational database by designing so that rows have primary keys and that they can't be null, this covers entity integrity. Referential integrity could be enforced by having checks for whether foreign keys exist in the foreign table. Domain integrity would be enforced through validation checks, this could be done backend validation, where we check the data type is the one we're expecting and if the input data is within the expected range e.g "age" shouldn't be a negative number.

#### References

- https://www.techopedia.com/definition/811/data-integrity-databases
- https://www.tutorialspoint.com/dbms/relational_data_model.htm

---

```
Q11.	Describe the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database. (100-200)
```

The manipulative aspects of the relational database model work through the use of Data Manipulation Language (DML) which is a sub-language of Structured Query Language (SQL).

DML allows one to use commands to manipulate data in the database, these commands can be applied on single or multiple records of a table. The main commands are:

- INSERT - used to insert values into the rows of a table by specifying table name and values to insert
- SELECT - used to retrieve or fetch records/rows from a table by specifying column names, table name and condition to select
- UPDATE - used to modify records by specifying table name, old column value, new column value and condition to update
- DELETE - used to remove records from a table by specifying table name and condition to delete

Relational databases may also be manipulated through the use of Object-relational mapping(ORM), which allows one to abstract tables into objects and manipulate them using their object-oriented language of choice. E.g ActiveRecord is an ORM framework in Ruby on Rails that allows us to abstract data into objects and retain the same create, read, update, delete (CRUD) functionality as DML, without having to write SQL.

#### References
- https://www.pluralsight.com/guides/sql-data-manipulation-language
- https://www.educba.com/data-manipulation-language/
- https://www.techopedia.com/definition/1179/data-manipulation-language-dml
- https://blog.bitsrc.io/what-is-an-orm-and-why-you-should-use-it-b2b6f75f5e2a
- https://guides.rubyonrails.org/active_record_basics.html
  
---

```
Q12.	Identify and explain the workings of TWO sorting algorithms and discuss and compare their performance/efficiency (i.e. Big O) (300-500)
```

**Bubble sort** - considered one of the simplest sorting algorithms, bubble sort works by comparing one element to the element adjacent to it and swapping them if they're out of place and then repeatedly doing this for subsequent elements. Bubble sort may need several passes of an array to properly sort all elements and it will also have to do a final pass to check that all elements are in order.

**Merge sort** - merge sort works by dividing the input data into sublists by dividing in half and then continually dividing the data into halves/sublists until it cannot anymore. It then reassembles each element into ordered sublists and then merges both halves to get the final sorted array. Merge sorts are known as a type of divide and conquer algorithm and are effective in sorting linked lists.

To compare the performance/efficiency of the two sorting algorithms we can compare their big O notation. A bubble sort has a Big O or worst time complexity of O(n _ n). This occurs when all elements in the array are sorted in reverse.<br>
Merge sort has a Big O of O(nLogn) which as you can see in the below picture doesn't rise as dramatically in complexity as input data increases.
Whereas O(n _ n) or O(n^2) quickly increases in complexity with input data size. So, initiallly, with small input data there may be a negligible difference between using either sort but as data input increases the poor performance of bubble sort becomes more apparent, in comparison to merge sort.

![bigochart](/docs/bigo2.png)

#### References

- https://www.geeksforgeeks.org/bubble-sort/
- https://www.geeksforgeeks.org/merge-sort/
- -image - https://www.bigocheatsheet.com/

---

```
## Q13.	Identify and explain the workings of TWO search algorithms and discuss and compare their performance/efficiency (i.e. Big O) (300-500)
```

**Linear search** - possibly the simplest search to implement and understand, the linear search has a time complexity of O(n) and involves looking at every element one after the other.

For example, for an array of 5 numbers a linear search would start at index 0 and check if the number is the one it was looking for and then continue moving up the index until it found it's number, or reached the end and concluded the number did not exist. A linear search could be used on an unsorted array as you may need to look at each element to see if it is the one we want.

**Binary search** - a binary search works by continually dividing the data in half until it finds the correct element. It usually requires the data to be sorted appropriately for it to be effective. An example to demonstrate this could be 5 numbers 10,35,68,90,100 sorted in ascending order and we wanted to find the number 100. A binary search would first attempt to take the mid-point of the input data and check if this value was the one we're looking for, in this case it would look at the last index, index 4, divide that in half to get 2, and then check if index 2 was 100. Since index 2 is 68 and not 100 it would then discard the lesser half of numbers and continue dividing and searching with the remaining data until the number was found or it concluded the number did not exist in the array.

In regards to the performance/efficiency of Linear search against Binary search, it may not be relevant to compare the two as they are best used for different purposes. Linear search would mainly be used on unsorted arrays as you need to look at each element to determine if it's the correct one, and Binary search requires an appropriately sorted array.
We can however compare the Big O notation of these searches to see if there is a difference in performance/efficiency.
Linear search's Big O notation or worst case is O(n), so as input data increases, it's time taken also increases linearly or directly proportional to input data.
Binary search, however, can be more efficient when you have the appropriately sorted array, at it's worst, it may have a Big O of O(logn) as input data grows, the complexity does not increase proportionally but logarithmically, which shows a curve complexity that flattens out as input data increases to infinity.

<br>
The below graph shows the Big O of "Linear Time" -green line, which is what Linear Search's big O would look like and "Logarithmic Time" - red line which is what Binary Search's big O would be.

![bigo](/docs/bigo.png)

#### References

- https://www.geeksforgeeks.org/linear-search/
- https://www.geeksforgeeks.org/binary-search/
- https://www.khanacademy.org/computing/computer-science/algorithms/binary-search/a/implementing-binary-search-of-an-array
- https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation/
- image - https://towardsdatascience.com/linear-time-vs-logarithmic-time-big-o-notation-6ef4227051fb

---

```
Q 14. 	Conduct research into a marketplace website (app) and answer the following parts:
a. List and describe the software used by the app.
```

- HTML
- CSS - styling of html
- Javascript
- jQuery
- React
- Java
- Amazon CloudFront - content delivery system
- Nginx - open source web server
- Bootstrap - framework for developing mobile-responsive designs
- Google cloud hosting - hosting of website
- Google analytics - marketing and traffic analysis
- Paypal / Visa - payment tools

<br>

Shown below is a fuller list of software used by the app - taken from stackshare

![gumtreestack](/docs/gumtreestack.png)

---

```
b. Describe the hardware used to host the app.
```

The hardware used to host Gumtree would be web/data servers using nginx as the web server software. The web server software would allow for HTTP requests for content from clients to be handled and addressed.
Gumtree also makes use of content delivery networks (Amazon CloudFront) and cloud hosting (Google Cloud hosting) which require a distributed network of servers.
The servers for Amazon CloudFront and Google Cloud hosting are geographically distanced. This allows these services to offer lower latency and travel time for regions closer to these servers.
In regards to cloud hosting, Gumtree uses Google Cloud hosting to make it's website scalable and reliable.

---

```
c. Describe the interaction of technologies within the app
```

Gumtree would be hosted through Google Cloud Hosting, a user would request content from the browser which would be sent as a HTTP request to nginx(webserver software). Nginx would send back a response which could be a mixture of HTML, CSS, javascript, jQuery and React, these technologies would form the basis for a responsive website. This response could also be passed to Amazon CloudFront which would attempt to send back the response from the server to the client through the most effective path.

---

```
d. Describe the way data is structured within the app
Describe (in general terms) the data structure of two-sided marketplace applications (e.g. eBay, Airbnb)
```

Data in a two-sided marketplace would typically be structured in a relational database model, that organizes our data and it's relevant relationships into relations. 

For example, for Gumtree we're going to need a User's table, a User could have the attributes of an Email (string data type), Password (encrypted string) and username (string). We could then make a table for Listings and define the relation between the Users table and Listings table. E.g A User can have zero or many Listings and a Listing belongs to a User.


```
e. Identify entities which must be tracked by the app
Identify entities which must be tracked by the application
```

In an application like Gumtree, entities that need to be tracked include:

- Users (email, password, name, ratings)
- Contact Details (user_id, email, location, phone number, listing_id)
- Listings (price, description, posting date, condition, price_options, contact details)
- Ratings (user_id, rating)
- Product Categories (category, description)
- Watchlist (listing_id, user_id )
- Messages (user_id, user_id2, messages)

Since GumTree generally assumes cash as payment and doesn't handle the fulfillment of listings, it doesn't keep any log of purchases. Users are expected to meet-up for the exchange of goods or trust that their product will be sent. It should also be noted you can place contact details on the user or different contact details in the listing itself.

---

```
f. Identify the relationships and associations between the entities you have identified in part (e)
```

* Users have zero or many listings
* Users have zero or many ratings
* Users have zero or many messages
* Users have zero or many listings on their watchlist
* Users have only one contact details

- Listings only have 1 Product Category
- Listings only belong to one User
- Listings only have one contact details
- Listings can belong to zero or many watchlists

* Messages only belong to one user

* Ratings only belong to one user

* Product Categories have zero or many listings

- Contact details can only have one user
- Contact details can belong to zero or many listings

* Watchlist can belong to one user
* Watchlist can have zero or many listings

---

```
g. Design a schema using an Entity Relationship Diagram (ERD) appropriate for the database of this website (assuming a relational database model)
```

Below is ERD for Gumtree

![gumtree erd](/docs/gumerd.png)


#### References

- 14a.
- https://stackshare.io/gumtree-com/gumtree-com
- https://builtwith.com/gumtree.com
- 14b.
- https://myip.ms/view/web_hosting/616098/Marktplaats_B_v.html
- https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server
- https://www.cloudflare.com/learning/cdn/what-is-a-cdn/
- https://www.wirehive.com/thoughts/cloud-hosting-work/
- 14e - g
- https://www.gumtree.com.au/
- https://www.gumtree.com.au/p-post-ad.html
---
