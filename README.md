# SHAREBILLS - ADVANCED DATABASE MANAGEMENT SYSTEM

Sharebill's mission is to make shared living and travel easier by providing neutral advice, fair judgement, and simplified expense sharing through Database management system. Inspired from the android/ios app 'Splitwise'.

<img src = https://user-images.githubusercontent.com/56169217/74609639-8f30e080-50b1-11ea-8092-3acabc33b6e2.png width = "350" height =              "350"/>

# DATABASE PLANNING

**1.	MISSION STATEMENT**

Sharebill's mission is to make shared living and travel easier by providing neutral advice, fair judgement, and simplified expense sharing through Database management system.

**2.	MISSION OBJECTIVES**

To maintain (INSERT, UPDATE, DELETE) DATA ON USERS
To maintain (INSERT, UPDATE, DELETE) DATA ON TRANSACTIONS
To maintain (INSERT, UPDATE, DELETE) DATA ON GROUPS
To maintain (INSERT, UPDATE, DELETE) DATA ON TRANSACTION_DETAIL
To maintain (INSERT, UPDATE, DELETE) DATA ON GROUP_MEMBERS
To maintain (INSERT, UPDATE, DELETE) DATA ON SETTLEUP_REQUEST
To perform searches on USERS
To perform searches on TRANSACTIONS
To perform searches on GROUPS
To perform searches on TRANSACTION_DETAIL
To perform searches on GROUP_MEMBERS
To perform searches on SETTLEUP_REQUEST
To track the status of settled transactions
To track status of transactions of Group members
To report the monthly transaction of a particular group.

**3.	STANDARDS DEVELOPMENT**

i.	The user should be a sharebills account holder 

ii.	Transactions such as Group or non-group transaction is allowed 

iii.	Any transaction can involve one or many users including himself

iv.	User (borrower) can send a Settle up request to another user (lender)

v.	User can include the limited users from the group members

vi.	User can take note of any number of users in the non-group transaction

vii.	Settle up request should be initiated by borrower and settle up should be done by lender only.

# DATABASE DESIGN

**4.	BUSINESS RULES**

• ShareBills is a database where transactions of all shared expenses between users is stored. 

•	ShareBills can get transactions from individual users and users from different groups.

•	Each user can be a part of none of the group or several groups.

•	Each group can have two or more users.

•	Every transaction involves two or more users. For example, Walmart expense is a transaction of common groceries with the amount of 200 USD that involved multiple users made on a particular day.

•	Each user can have zero or many transactions.

•	For each user there is zero settle up request or many settle up requests.

•	Every user is identified by User ID. The first name, last name, middle name, email id, and phone number of all users are recorded in the system. 

•	A borrower can send a settle up request to lender once he repays the amount lent from borrower. Once the lender approves the settle up request, the rows in the Transaction detail entity will be updated.

•	Transaction detail entity has information about transaction id, borrower id, debt amount, settled up flag, and settle up request id. 

•	For every group, group id, group name and group created date is maintained.

•	For every single settle up request is known by Request id. In addition, request made by a user, request sent to a user with the request status, request received date, request accepted date, and request group id is stored in the system.

•	A particular transaction is recognized by transaction id. Transaction owner id, Lender id along with the transaction group id, transaction date, transaction amount, and a transaction comment are also kept in the database.

**5.	ERD DIAGRAM**

![share](https://user-images.githubusercontent.com/56169217/74609682-08c8ce80-50b2-11ea-926b-adeb3dbda488.png)


Pleasr refer the SQL queries written in MYSQL: 

