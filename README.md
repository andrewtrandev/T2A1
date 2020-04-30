
https://coderacademy.instructure.com/courses/288/assignments/1464

## Q1.	Describe the architecture of a typical Rails application







---
## Q2.	Identify a database management system (DBMS) commonly used in web applications (including Rails) and discuss the pros and cons of this database

ACME Corporation is very big on project management, documentation and process. This will be a key metric in their decision to award the project. The following set of questions relate to this RfQ-requirement.





---
## Q3. Discuss the implementation of Agile project management methodology (200-300) 
Discuss questions -require an in-depth answer that takes into account all aspects of the debate concerning a topic.
Why choose the agile method versus alternatives such as the waterfall method?


The Agile methodology was developed with the goal of improving software development. Agile's four main values are an emphasis 
on 
* Valuing individuals and interactions over processes and tools
* Developing working software versus documentation 
* Collaborating with customers versus contract negotiation
* Quickly responding to change versus following a plan

The Agile methodology advocates developing projects and software through constant iteration and collaboration to address the needs of customers.  

It may be useful to compare the Agile and Waterfall methodology as they're both used in project management but under different circumstances. 

In the past software was mainly developed through the waterfall methodology, at the time it was a useful way to develop software as requirements and technology were slow in changing. It was also easy to understand and follow as each phase had clear goals. Customers were only involved at the start and end of a project. This could lead to issues such as customer's needs changing which are usually expensive to address due to rewriting of projects and code.

In contrast, in Agile, customers are constantly involved throughout the development of the project and their feedback can be quickly incorporated into the project. Agile also relies on short sprints or cycles that involve designing, building, testing and review. These cycles can repeat and this is in contrast to the waterfall method which generally has longer time periods and non-repeating phases.

Below is an example of a 3 cycles or sprints linking together.
![agile loop](docs/loop.png)


In today's age with the rapid development of start-ups and software, organisations have to be flexible and quick to respond to customer's needs. The agile method caters to this need by allowing for rapid prototyping and development of software, this allows customers to examine the progress of software development quickly, in contrast to the waterfall methodology, in which, projects may take years before they have a product to show.


### References     
https://www.agilealliance.org/agile101/12-principles-behind-the-agile-manifesto/
    
https://www.infoworld.com/article/3237508/what-is-agile-methodology-modern-software-development-explained.html

https://www.guru99.com/waterfall-vs-agile.html

https://www.projectmanager.com/software/use-cases/waterfall-methodology

https://www.mendix.com/blog/agile-process-why-you-need-feedback-loops-both-during-and-after-sprints/

## Q4.	Provide an overview and description of a standard source control workflow





---
## Q5.	Provide an overview and description of a standard software testing process (e.g. manual testing)


Companies (including ACME Corporation) value previous project experience and case studies. The following set of questions relate to this RfQ-requirement.





---

Having suffered several cyber attacks in the past and resultant remedial audits ACME Corporation takes compliance, security and privacy very seriously. The following set of questions relate to this RfQ-requirement.

## Q6.	Discuss and analyse requirements related to information system security and how they relate to the project

Discuss - for and against
Analyse - break the essay topic down into fundamental parts



## Q7. Discuss common methods of protecting information and data and how you would apply them to the project

A common method of protecting information and data would be to implement authentication, this could be done through the use of a gem such as Devise to require users to have a login and password before they could access the application. A benefit of authentication is this would protect personal user data and information in a quick and simple way. Cons of using a user login system, is that it's up to users to be vigilant with their passwords and to also generate complex and unique passwords.

We could also implement authorisation as a method to protect data, this would restrict the permissions of users. For example we would only want users to be able to change their contact details and not someone else's. This also ties into the principle of giving entities the fewest privileges possible. For example an admin may have the power to remove a user but we would disable that function for anyone who wouldn't require it e.g a user or even an employee. This reduces our risk to vulnerabilities because if you gave that permission to users or employees who didn't require it, they also become points of failure.


Ref
* https://www.keycdn.com/blog/web-application-security-best-practices
* https://www.synopsys.com/blogs/software-security/complete-web-application-security-testing-checklist/

---
## Q8.	Research what your legal obligations are in relation to handling user data and how they can be met for the project





---
## Q9.	Describe the structural aspects of the relational database model. Your description should include information about the structure in which data is stored and how relations are represented in that structure.




---
## Q10.	Describe the integrity aspects of the relational database model. Your description should include information about the types of data integrity and how they can be enforced in a relational database.





---
## Q11.	Describe the manipulative aspects of the relational database model. Your description should include information about the ways in which data is manipulated (added, removed, changed, and retrieved) in a relational database.

---
## Q 14. 	Conduct research into a marketplace website (app) and answer the following parts:  
 ### a. List and describe the software used by the app.
Conducts research and describes the software used by an organisation (software / database)

Gumtree uses a mix of HTML, CSS, Javascript, jQuery, React and Java in it's app. It uses AmazonCloudFront as a content delivery system and does this over nginx which is an open source web server. Gumtree also utilises Bootstrap as a framework for developing mobile-responsive designs. Other notable software include Paypal and Visa for payments and google analytics for marketing/analysis.



Shown below is a fuller list of software used by the app - taken from stackshare
![gumtreestack](/docs/gumtreestack.png)




 ### b. Describe the hardware used to host the app.
Conducts research and describes the infrastructure used by an organisation (hardware / networks) -Shows a full understanding of the hosting infrastructure

The hardware used to host Gumtree would be web/data servers using nginx as the web server software. The web server software would allow for HTTP requests for content from clients to be handled and addressed.
Gumtree also makes use of content delivery networks and cloud hosting which require a distributed network of servers. Specifically the servers for a content delivery network are geographically distanced while for cloud hosting the data is stored on different servers.
In regards to cloud hosting, Gumtree uses Google Cloud hosting 
#############Add in google hosting

 ### c. Describe the interaction of technologies within the app
Describes the interaction of technologies and identifies their role and purpose in the system

A client would request content from the browser which would be sent as a HTTP request to nginx(webserver software). Nginx would send back a response which could be a mixture of HTML, CSS, javascript, jQuery and React, these technologies would form the basis for a responsive website. This response could also be passed to Amazon CloudFront which would attempt to send back the response from the server to the client through the most effecive path.



 ### d. Describe the way data is structured within the app
Describe (in general terms) the data structure of two-sided marketplace applications (e.g. eBay, Airbnb)




 ### e. Identify entities which must be tracked by the app
Identify entities which must be tracked by the application



 ### f. Identify the relationships and associations between the entities you have identified in part (e)
Identifies all relationships / associations in a sophisticated relational model



 ### g. Design a schema using an Entity Relationship Diagram (ERD) appropriate for the database of this website (assuming a relational database model)

 Designs a normalised schema (i.e. without data duplication) that facilitates extended functionality of the app


 Refs

* 4a.
* https://stackshare.io/gumtree-com/gumtree-com
* https://builtwith.com/gumtree.com
* 4b.
* https://myip.ms/view/web_hosting/616098/Marktplaats_B_v.html
* https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server
* https://www.cloudflare.com/learning/cdn/what-is-a-cdn/
* https://www.wirehive.com/thoughts/cloud-hosting-work/



