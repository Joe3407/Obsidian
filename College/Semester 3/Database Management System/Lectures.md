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
## 📘Lec 2

- **ER (Entity–Relationship) Model Concepts:**
	- **Entities:** It may be an object with a physical existence (a particular person, car), or with a conceptual existence (a company, a job, or a university course)
	- **Attributes:** They are properties used to describe an entity, e.g. an EMPLOYEE entity may have the attributes Name, SSN, Address, Sex
- **Types of Attributes:**
	- **Simple:** Single atomic value, e.g. SSN, Sex 
	- **Composite:** Composed of several components, e.g. Address(Street, City, Zip code, Country), Name(First name, Middle name, Last name)
	
	- **Single-valued:** Contains one value for one attribute, e.g. Name, Sex, Age
	- **Multi-valued:** Contains several values for one attribute, e.g. Car Color(Red, Black)
	
	- **Stored:** `Birth_date` 
	- **Derived:** The Age attribute is called a derived attribute and is said to be derivable from the `Birth_date` attribute
- **Entity Types:**
	- **Key Attribute:** It's the attribute which is unique for the entity, e.g. Name, Id 
	- **Strong Entity:** Contains key attribute
	- **Weak Entity:** Doesn't contain any key attributes 
- **Initial Design of Entity Types:** It contains the entities and their attributes with their relation as attributes 
- **Entity Set:** It's the collection of all CAR entity instances currently stored in the database
- **Relationship:** An association between two or more entities with a specific meaning
- **Relationship Type:** It's the name of the relation between two entities, e.g. `WORKS_FOR` 
- **Relationship Instance:** e.g. `John` $\to$ `WORKS_FOR` $\to$ `IT`, this is one instance
- **Relationship Set:** It's the current relations stored in the database 
  
- **ER Diagram Representations:**

| Symbol Type | Text Notation | Visual Description |
| :--- | :--- | :--- |
| **Entity** | `[Entity]` | Rectangle |
| **Weak Entity** | `[[Weak Entity]]` | Double Rectangle |
| **Relationship** | `<Relationship>` | Diamond |
| **Identifying Relationship** | `<<Identifying Rel>>` | Double Diamond |
| **Attribute** | `—(attribute)` | Oval with line |
| **Key Attribute** | `—(underline)` | Underlined Oval |
| **Multivalued Attribute** | `—((attribute))` | Double Oval |
| **Composite Attribute** | `—(attr1, attr2...)` | Connected Ovals |
| **Derived Attribute** | `- -(attribute)- -` | Dashed Oval |

-  **Relationship & Constraint Notation:** 

| Constraint Type             | Text Notation       | Description                                      |
| :-------------------------- | :------------------ | :----------------------------------------------- |
| **Total Participation**     | `E1 — <R> == E2`    | Double line means total participation of E2 in R |
| **Cardinality Ratio (1:N)** | `E1 —1< R >N— E2`   | 1 to N relationship between E1 and E2            |
- **Notes:** 
	- **Weak Entity:** It's in a double Rectangle, and must have a relation with double diamond and connected to an entity
	- **Dashed Underline:** It's in the weak entity when we want to identify an object so we use the key attribute in the Entity and this dashed lined attribute in the weak entity 

---
## 📘Lec 3

- **Recursive Relationship:** Having same entity but with two different roles, e.g. `SUPERVISION`, it contains supervisor and supervisee, which both are different roles but with the same entity 
- **Weak Entity:**
	- **Overview:** 
		- An entity that doesn't have a key attribute
		- It must participate in an identifying relationship with a strong/owner/identifying entity type
		- It always has a total participation constraint (existence dependency) with respect to its identifying relationship, meaning it contains a double line connections as it's mandatory 
	- **Entity Identifying:** An entity is identified by a Partial Key (underlined with dots), and the particular entity they are related to 
- **Constraints on Relationships:**
	- **Cardinality Ratio:**
		- **Meaning:** It tells you the maximum number of entities that can be associated with another entity
		- **Types:** 1:1, 1:N, N:1, M:N
	- **Participation Constraint:**
		- **Total Participation:** Every entity of that type must participate in at least one instance of the relationship. Represented by a double line in an ER diagram
		- **Partial participation:** An entity may participate zero times. Represented by a single line
	- **(min, max) Notation:**
		- Read the (min, max) numbers next to the entity type and looking away from the entity type
		- **Minimum:** It shows the Participation Constraint, min=0 then it's partial participation, min>0 then it's total participation 
		- **Maximum:** It shows the Cardinality Ratio 
- **ER-to-(Relational/Schema) Mapping:**
	- **Overview:**
		- **ER Diagram:** Describes what data exists and how the data is related
		- **Relational Schema:** Describes how that data is organized into tables
		- **ER-to-Relational Mapping:** The rules that take you from the ER Diagram to the Relational Schema
	- **Steps:**
		- **Mapping of Strong Entities:**
			- Create a relation (table) that includes all the simple attributes of entity
			- Choose one of the key attributes as the **Primary Key** 
			- All composite attributes are written as simple attributes, e.g. `First_name` & `Last_name` both are written without `name` 
			- If the chosen key is composite, the set of simple attributes that form it will together form the primary key
		- **Mapping of Weak Entities:**
			- Create a relation (table) that includes all the simple attributes of entity
			- Include a foreign key that contains a combination of partial key from the weak entity and primary key from strong entity

---
