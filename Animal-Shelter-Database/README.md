# Pawradise Animal Shelter: Database Management System (Oracle SQL)

A relational database designed for a fictional Malaysian NGO animal shelter that houses 50+ cats and dogs. It replaces scattered records with one structured system for animals, adoptions, staff tasks, veterinary care, volunteers and donations.

> Group project for SEG1201 Database Fundamentals, Sunway University (2025). Group 6_3, 5 members.
> 🎥 Video demo: https://youtu.be/ODEaA4v5D-E

## Problem
The shelter struggled to track animal health, adoption records, staff and volunteer duties, vet history and donors. We designed a database to keep all of it consistent and queryable.

## Database design
**Entities (14 tables):** Animal, Category, Animal Category, Adopter, Adoption, Staff, Task, Staff Duty, Veterinary, Volunteer, Volunteer Duty, Donor, Donation

- Business rules defined for each entity
- ERD drawn with and without constraints
- Normalised relational model with primary and foreign keys
- Constraints: `NOT NULL`, `UNIQUE`, `CHECK`, and FK integrity

![ERD](images/erd.png)

## SQL queries implemented
| # | Requirement | What it answers |
|---|---|---|
| a | Outer join | All animals plus adoption info and adopter name (if adopted) |
| b | 4+ table join with `GROUP BY` | How many volunteer duties each staff member supervised, by task |
| c | `LIKE` pattern + date functions | Volunteers whose names contain "ah" and their duties in July 2024 |
| d | `AND` + `OR` | Staff doing health monitoring, record tracking or quarantine duty, Feb–Jun 2024 |
| e | 2+ subqueries | Adult cats that haven't been adopted yet |
| f | Scenario question | Animals in the shelter for over a year with the best health ratings |

## Repository contents
```
├── sql/
│   ├── 01_create_tables.sql
│   ├── 02_insert_data.sql
│   └── 03_queries.sql
├── images/
│   ├── erd.png
│   └── relational_model.png
├── docs/
│   └── Animal_Shelter_Report.pdf
└── README.md
```

## How to run
1. Open Oracle SQL Developer (or Oracle Live SQL).
2. Run `01_create_tables.sql`, then `02_insert_data.sql`.
3. Run any query in `03_queries.sql`.

## My contribution
I validated the table creation and insert scripts (data types, foreign key issues, data matching the structure across tables), wrote and presented queries (a)–(c), and formatted the final report.

## Team
Low Kit Ian · Chai Ze Yan · Tan Jia Ying · Toh Ver Niel · Yong Tze Shuen
