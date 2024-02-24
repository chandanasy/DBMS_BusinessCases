This Repository includes different business case scenarios and corresponding data models created to address business requirements. The aim was to improve data management and analytics capabilities, leading to a more efficient query process and enhanced data integrity.

## NYC Transit Business Case 



### Overview
This business case focuses on the New York City Subway system, with an emphasis on organizing and structuring data to improve operational efficiency and service analysis. The design employs a relational database model to capture intricate details of subway lines, stations, operations, and facilities.

### Assumptions Made
To address the complexities of the NYC Subway system and ensure a robust database design, the following assumptions have been made:

- **CSY_TR (Train Line Data/Attributes):** Each train line has unique attributes, including line number/name, division, and operational years.

- **CSY_SS (Subway Station Data/Attributes):** Each subway station is identified by a unique name and address, associated with a specific borough and neighborhood.

- **CSY_SOP (Subway Operations Data/Attributes):** Operations data captures details of train lines at subway stations, including arrival and departure times and service types (local/express/mixed).

- **CSY_SF (Subway Station Facilities Data/Attributes):** Facilities at each station, such as elevators, escalators, restrooms, are recorded, with attributes indicating their availability (Yes/No).

- **CSY_TRSS (Associative Entity):** This associative table resolves the many-to-many relationship between train lines (CSY_TR) and subway stations (CSY_SS).

#### Specific Assumptions:
a. Each station has a unique set of facilities.
b. Missing arrival/departure times in operations data are handled programmatically, not within the database constraints.
c. A one-to-one relationship exists between subway stations (CSY_SS) and their facilities (CSY_SF), assuming each station's set of facilities is unique.
d. A many-to-many relationship is defined between train lines (CSY_TR) and subway stations (CSY_SS) — a train line can pass through multiple stations, and each station can serve multiple train lines.
e. One-to-many relationship from train lines (CSY_TR) to operations (CSY_SOP) — each train line can have multiple operations.
f. One-to-many relationship from subway stations (CSY_SS) to operations (CSY_SOP) — each station can have multiple operations.
g. One-to-one relationship from subway stations (CSY_SS) to facilities (CSY_SF) — each station has a specific set of facilities.

### Model and SQL Code
The database schema, along with its constraints and relationships, is defined in the DDL code provided. 
