## 📘Lec 1 

- **Database:** A collection of related data 
- **Transaction:** Multiple database accesses, but together they form one transaction, e.g. Transfer $100 from Ahmed → Joe
- **📝Types of Databases:** 
	- **Traditional:** Stores textual or numeric information
	- **Multimedia:** Stores images, audio clips, and video streams digitally
	- **Geographic Information Systems (GIS):** Can store and analyze maps, weather data, and satellite images
	- **Data warehouses & Online Analytical Processing (OLAP):** They're used to Extract and analyze useful business information from very large databases to support decision making
	- **Real-time:** It uses real-time processing to handle workloads whose state is constantly changing, e.g. a stock market changes very rapidly and is dynamic
- **📝Database Management System (DBMS):** Software used to create, maintain, and manipulate databases
- **Database System:** The **DBMS + the actual database (data)**. It represents the whole setup used to store and manage the data 
- **Data Model:** A set of concepts to describe **Structure** (What? Tables, Entities), **Constraints** (Rules? GPA 0-4), **Operations** (What can I do? Insert, Delete)
- **📝Categories of Data Models:** 
	- **Conceptual:** What data and relationships exist,           We need students, courses, professors
	- **Logical:** How is the data organized logically                Let's represent them using these tables
	- **Physical:** How is it actually stored in the computer      Let's actually store those tables using these storage structures
- **📝Database State/Instance:** Refers to the content of a database at a moment in time
- **Initial Database State:** Refers to the database state when it is initially loaded with the initial data into the system
- **Valid State:** A state that satisfies the structure and constraints of the database
- **Data Definition Language (DDL):** Defines the structure, "What does my database look like?"
- **Data Manipulation Language (DML):** Manipulates the data, "What do I want to do with the data?"
- **Centralized DBMS:** Everything is in one system
- **Client-Server DBMS:** Clients ask servers to provide services

---
