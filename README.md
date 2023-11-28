# IS620proj

Team members:  

1 - Nihant Malempet
2 - Chaitanya Shetty
3 - FNU Ayesha
4 - Aswin Kumar Janakiraman
5 - Kush Patel
6 - Ashutosh Latwala


Team Suicide Sqaurd.
![image](https://github.com/kushptl1/IS620proj/assets/150859750/9e062a31-49a1-4904-adba-016609767ccc)


**Title:** Online Marketplace Database and Operations Development

**Overview:** Our team has been contracted to build the software and database backend for a new online marketplace aiming to compete with the likes of Amazon and Walmart.

The scope includes designing a robust Oracle database, defining schema, and developing PL/SQL procedures for core marketplace operations like managing product listings, storing customer information, enabling ordering, generating invoices, providing personalized recommendations, and producing business intelligence reports.

The work will be executed by a cross-functional team dividing responsibilities across critical phases:

Database and Schema Design
Define logical and physical schema
Normalize structure for flexibility and speed
Core Operations Procedures
Add/update/delete product listings
Securely store and manage customer accounts
Facilitate order processing and billing
Analytics Procedures
Produce reports on sales, revenue, product performance
Develop recommender system for personalized suggestions
Testing and Deployment
Devise test plans
Fix bugs
Deploy to production

**Project Delivery:** The project will be delivered iteratively based on milestones focused on database, operations, and analytic modules. Team members will collaborate on design documentation while owning individual development procedures later consolidated via code reviews.

**ERD:**

![ER Diagram](https://github.com/kushptl1/IS620proj/assets/150859992/3d79b746-90f2-4135-b254-79f55a37eb43)

The above diagram is the entity relationship diagram for our project.
In our project, E-R Diagram mainly contains the entities such as Customer, Credit_Cards, Product_Category, Invoices, Orders, Products, Recommendations and Review, as you can see above.

The attributes of all the entities are as follows.

Customer
	Customer_ID (Primary Key)
	F_Name
	L_Name
	Email
	City
	State
	Zip
	
Credit_Cards
	Card_number (Primary Key)
	Customer_ID (Foreign Key)
	Card_type
	Expiration_year
	Expiration_month

Product_Category
	ProductCategory_ID (Primary Key)
	ProductCategory_Name
	ProductCategory_Desc

Invoices
	Invoice_ID (Primary Key)
	Order_ID (Foreign Key)
	Customer_ID (Foreign Key)
	Card_Number (Foreign Key)
	Amount

Orders
	Order_ID (Primary Key)
	Customer_ID (Foreign Key)
	Product_ID (Foreign Key)
	Quantity
	Order_Date

Products
	Product_ID (Primary Key)
	ProductCategory_ID (Foreign Key)
	Product_Name
	Avail_Quant
	Unitprice

Recommendation
	Recommendation_ID (Primary Key)
	Customer_ID (Foreign Key)
	RecommendedProduct_ID
	Recommendation_Date

Review
	Review_ID (Primary Key)
	Product_ID (Foreign Key)
	Reviewer_email
	Stars_Given
	Review_Text

The Customer and Credit_Cards entities have one to many relationship. Here, the single customer can have a multiple credit cards whereas single credit card cannot belong to multiple customers.

The Customer and Orders entities have one to many relationship. As one customers can have many orders and individual order belongs to one customer only.

The Orders and Invoices entities have one to one relationship. It is obvious that the individual order can have only one invoice.

The Customer and Invoices entities have one to many relationship. Here, one customer can have multiple invoices based on his/her order but the same invoice cannot belong to many customers.

The Orders and Products entities have many to many relationship. As, one order can have multiple products similarly one product can belong to many orders and many orders can have many products.

The Products and Product_Category entities have many to one relationship. Here, single category can have multiple products but single product can not belong to many categories.

The Products and Review entities have many to many relationship. Multiple products can have multiple reviews from multiple customers.

The Products and Recommendations entities have many to many relationship. Multiple products can have multiple recommendations from multiple customers.

The Recommendations and Customer entities have many to many relationship. As single customer can give many recommendations. Similarly one kind of recommendation can also given by multiple customers. Hence, multiple recommendations can belong to many customers.

Hence, the E-R Diagram basically provides a foundation for design and development of an Online Shopping DB System.
