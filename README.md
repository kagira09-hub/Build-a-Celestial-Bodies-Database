# Build-a-Celestial-Bodies-Database
# Celestial Bodies Database 🌌

## Project Overview

This project is part of a relational database design exercise using **PostgreSQL**.
The goal is to design and build a **Universe database** that models relationships between celestial bodies such as galaxies, stars, planets, and moons.The project demonstrates key database concepts including:

* Table creation
* Primary and foreign keys
* Data types
* Table relationships
* Data integrity constraints

# Database Setup

1. Log into PostgreSQL using:

psql --username=freecodecamp --dbname=postgres

2. Create the database:

CREATE DATABASE universe;

3. Connect to the database:
   
\c universe

# Database Structure

The database models a simplified universe consisting of several related entities.

## Core Tables

The database contains the following main tables:

**galaxy**
**star**
**planet**
**moon**

An additional table may be added to meet the minimum table requirement.

# Table Requirements
## Primary Keys

* Each table must contain a **primary key**.
* All primary keys must **auto-increment**.
* Primary keys must follow the naming convention:

table_name_id

Example:

moon_id
planet_id
star_id
galaxy_id

## Columns

Each table must meet the following conditions:

* Each table must contain a **name column**
* All `name` columns must use the **VARCHAR** data type
* Each table must contain **at least three columns**
* The tables `galaxy`, `star`, `planet`, and `moon` must each contain **at least five columns**

## Data Types

The database must demonstrate the use of several PostgreSQL data types:

* **INT** → at least two columns that are not primary or foreign keys
* **NUMERIC** → used at least once
* **TEXT** → used at least once
* **BOOLEAN** → used in at least two columns

## Constraints

Each table must include:

* At least **two columns that do not allow NULL values**
* At least **one UNIQUE column**

These constraints help maintain **data integrity and prevent duplicates**.

# Table Relationships

The project models hierarchical relationships between celestial bodies.

### Galaxy → Star

Each **star** must reference a **galaxy**.

star.galaxy_id → galaxy.galaxy_id

### Star → Planet

Each **planet** must reference a **star**.

planet.star_id → star.star_id


### Planet → Moon

Each **moon** must reference a **planet**.

moon.planet_id → planet.planet_id

# Minimum Data Requirements

Each table must contain a minimum number of rows:

| Table      | Minimum Rows |
| ---------- | ------------ |
| galaxy     | 6            |
| star       | 6            |
| planet     | 12           |
| moon       | 20           |
| all tables | at least 3   |

# Total Tables

The database must contain **at least five tables**.

# Example Database Relationships

Galaxy
   ↓
Star
   ↓
Planet
   ↓
Moon

This structure demonstrates **one-to-many relationships** between celestial bodies.

# Purpose of the Project

This project is designed to practice:

* Relational database design
* Primary and foreign key relationships
* Data normalization
* PostgreSQL table creation and constraints

# Technologies Used

* PostgreSQL
* psql CLI
* SQL
  
# Author
Created as part of the **Relational Database Certification Project**.
