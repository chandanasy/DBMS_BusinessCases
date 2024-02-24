# Business Case Scenarios Data Models

This repository includes different business case scenarios and corresponding data models created to address specific business requirements. The aim was to improve data management and analytics capabilities, leading to a more efficient query process and enhanced data integrity.

---

## NYC Transit Business Case

### Overview
This business case focuses on the New York City Subway system. It aims to restructure data to improve operational efficiency and facilitate service analysis through a relational database model that captures details of subway lines, stations, operations, and facilities.

### Assumptions Made
Several assumptions underpin the database design for the NYC Subway system:

- **Train Line Data/Attributes (CSY_TR):** Each train line has unique identifiers, divisions, and operational timelines.
- **Subway Station Data/Attributes (CSY_SS):** Stations are uniquely defined by name and location, tied to boroughs and neighborhoods.
- **Subway Operations Data/Attributes (CSY_SOP):** Details include train line, station, service times, and type.
- **Subway Station Facilities Data/Attributes (CSY_SF):** Records facility availability at stations.
- **Associative Entity (CSY_TRSS):** Resolves many-to-many relationships between train lines and stations.

#### Specific Assumptions:
- Unique facilities per station.
- Programmatic handling of missing time data.
- One-to-one relationship for station facilities.
- Many-to-many relationship for train lines and stations.
- One-to-many relationships for train lines to operations and stations to operations.
- One-to-one relationship from stations to facilities.

### Database Design
The database schema, along with its constraints and relationships, is detailed in the provided DDL code.

---

## Uber Eats Database Design Project

### Business Case
The Uber Eats database design reflects the operational needs of an expansive food delivery service operating across multiple countries and thousands of cities.

### Assumptions Made
The database design is predicated on the following assumptions:

- **Courier Data (CSY_COURIER):** Personal and vehicle-related information of the courier is stored, with constraints on banking details to reflect standard sizes.
- **Customer Data (CSY_CUST):** Customers are identified by personal information and classified by type.
- **Restaurant Data (CSY_REST):** Restaurants are listed with contact details and specialties, with optional website URLs.
- **Delivery Service Data (CSY_DEL):** Delivery transactions record detailed order and payment information.
- **Associative Table (CSY_CC):** Manages many-to-many relationships between restaurants and delivery services.

### Entity Relationships
- Direct associations between delivery orders, restaurants, couriers, and customers.
- One-to-many relationships are defined for couriers, customers, and restaurants with delivery services.
- A many-to-many relationship exists between couriers and customers, facilitated by an associative table.

### Database Design
The database schema encapsulates entities, attributes, and relationships as per the assumptions. Oracle Data Modeler was used to create both logical and relational models. The DDL code provided enables the execution of the database schema as designed.

---

## Contributing
Contributions to the repository are welcome. If you have suggestions for improving the database designs or adding new business cases, please submit a pull request with your proposed changes.

## Usage Notes
Please ensure compliance with all relevant data use policies and privacy considerations when applying these database designs in real-world applications. Detailed instructions for the database design process are included within the SQL scripts and model diagrams for each business case.

