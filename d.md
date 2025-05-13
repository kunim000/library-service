# Library Management System

A complete suite of book lending system with role based features : 
*(Check [Snapshots](#snapshots))*
1. Admin
    * Add books with isbn validation and inventory creation with unique id & generating downloadable (pdf) barcode.
    * Search, update and delete books or inventory.
    * Add, search, update and delete users.
    * Search orders based on order id, user id or book id.
    * Mark order as collected.
    * Mark order as returned and generate downloadable invoice with late fees as applicable.
    * Search user's order history.
    * Search orders that are overdue for return by user id or book id.

2. User
    * Order a new book based on inventory availability.
    * Search self orders and order history.
    * Filter orders based on return overdue.

3. All
    * Authentication with Login and Logout.
    * Role based authorization and views (front-end).
    * Update self account details & change password.
    
## Technology Stack & Frameworks
> `Java 11`  `Spring-Boot-2.3.4.RELEASE` `Spring-Cloud-Hoxton.SR8` `Spring-Security` `Spring Data JPA` `Vue JS 2` `Vuetify 2.4` `Docker` `Docker-Compose` `JUnit 5`

## Installation and Running
- **With Docker and Docker Compose Installed**
```docker
docker compose down
docker compose build
docker compose up
-------------------------
or run the start.sh file
-------------------------
./start.sh
```
