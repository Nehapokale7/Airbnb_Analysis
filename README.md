## Airbnb Data Analysis Project Using SQL

### 1. Project Overview

The **Airbnb Data Analysis Project** focuses on analyzing Airbnb listing data to extract meaningful business insights using **SQL**. The project helps understand pricing patterns, host behavior, availability trends, and customer preferences, which are crucial for decision-making in the hospitality and rental market.

---

### 2. Objectives

* Analyze Airbnb listings to understand price distribution across locations
* Identify top-performing neighborhoods and room types
* Study host activity and listing frequency
* Analyze availability trends and booking patterns
* Extract insights that help optimize pricing and improve customer experience

---

### 3. Dataset Description

The dataset contains Airbnb listing information with the following key tables/columns:

**Listings Table**

* `id` – Unique listing ID
* `name` – Name of the listing
* `host_id` – Unique host identifier
* `host_name` – Name of the host
* `neighbourhood` – Area where the property is located
* `room_type` – Type of room (Entire home, Private room, Shared room)
* `price` – Price per night
* `minimum_nights` – Minimum nights required for booking
* `availability_365` – Number of available days in a year

**Reviews Table (if applicable)**

* `listing_id` – Listing ID
* `review_date` – Date of review

---

### 4. Tools & Technologies Used

* **Database:** MySQL / PostgreSQL
* **Language:** SQL
* **IDE/Tool:** MySQL Workbench / pgAdmin
* **Data Source:** Airbnb open dataset

---

### 5. Key SQL Operations Used

* `SELECT`, `WHERE`, `ORDER BY`, `GROUP BY`
* Aggregate functions: `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`
* Joins (`INNER JOIN`, `LEFT JOIN`)
* Subqueries
* Views
* Date functions

---

### 6. Analysis Performed & Sample Queries

#### a. Total Number of Listings

```sql
SELECT COUNT(*) AS total_listings FROM listings;
```

#### b. Average Price by Room Type

```sql
SELECT room_type, AVG(price) AS avg_price
FROM listings
GROUP BY room_type;
```

#### c. Top 10 Most Expensive Neighborhoods

```sql
SELECT neighbourhood, AVG(price) AS avg_price
FROM listings
GROUP BY neighbourhood
ORDER BY avg_price DESC
LIMIT 10;
```

#### d. Host with Maximum Listings

```sql
SELECT host_name, COUNT(*) AS total_listings
FROM listings
GROUP BY host_name
ORDER BY total_listings DESC
LIMIT 1;
```

#### e. Availability Analysis

```sql
SELECT neighbourhood, AVG(availability_365) AS avg_availability
FROM listings
GROUP BY neighbourhood;
```

---

### 7. Key Insights

* Entire homes/apartments have the highest average price compared to other room types
* Certain neighborhoods consistently show higher demand and pricing
* A small number of hosts manage multiple listings
* Listings with higher availability tend to have competitive pricing

---

### 8. Business Impact

* Helps hosts optimize pricing strategies
* Assists customers in choosing cost-effective locations
* Enables Airbnb to identify high-demand areas
* Supports data-driven decision-making for property investments

---

### 9. Conclusion

This project demonstrates effective use of **SQL for data analysis**, showcasing skills in querying, aggregating, and interpreting large datasets. The insights derived can help improve operational strategies and customer satisfaction in the Airbnb ecosystem.

---

### 10. Skills Demonstrated

* SQL querying & optimization
* Data cleaning and aggregation
* Analytical thinking
* Business insight generation

---

*This project can be used for academic submissions, internships, or portfolio presentations.*

## GitHub README.md

# Airbnb Data Analysis Using SQL

## 📌 Project Overview

This project focuses on analyzing **Airbnb listing, host, booking, and review data** using **SQL** to uncover meaningful business insights. The database is designed with normalized tables and realistic relationships to simulate a real-world Airbnb analytics environment.

The analysis helps understand:

* Pricing patterns across neighborhoods
* Host performance (Superhost vs Regular hosts)
* Booking trends and revenue behavior
* Impact of amenities on pricing and ratings
* Occupancy and stay duration patterns

---

## 🛠️ Tech Stack

* **Database:** MySQL
* **Language:** SQL
* **Tools:** MySQL Workbench / phpMyAdmin
* **Dataset Type:** Synthetic Airbnb-style dataset

---

## 🗂️ Database Schema

The project consists of the following tables:

* `hosts` – Host details and performance metrics
* `neighborhoods` – Geographic and location data
* `listings` – Property and pricing information
* `amenities` – List of available amenities
* `listing_amenities` – Mapping between listings and amenities
* `reviews` – Guest reviews and ratings
* `bookings` – Booking history and revenue details

All tables are connected using **primary and foreign keys** to maintain referential integrity.

---

## 📊 Key Analysis Performed

### 1. Neighborhood Performance Analysis

* Average daily rate by neighborhood
* Booking frequency per listing
* Average stay duration

### 2. Host Performance Comparison

* Superhost vs Non-Superhost comparison
* Average pricing, ratings, bookings, and revenue

### 3. Booking & Revenue Trends

* Monthly booking patterns (2023)
* Total revenue and average booking value
* Average length of stay

### 4. Amenities Impact Analysis

* Effect of amenities on pricing
* Relationship between amenities and guest ratings

### 5. Host Responsiveness Analysis

* Impact of host response time and rate on bookings and ratings

### 6. Pricing Strategy Evaluation

* Identification of **Underpriced**, **Overpriced**, and **Fairly Priced** listings using Z-score analysis

### 7. Predictive Trend Analysis

* Historical monthly trends
* Estimation of future booking behavior based on past data

---

## 🧪 Sample Insights

* Entire homes have higher average prices than private rooms
* Superhosts generate higher revenue and better ratings
* Listings with more amenities tend to have higher prices and ratings
* Certain neighborhoods consistently outperform others
* Host responsiveness strongly influences booking success

---

## ▶️ How to Run the Project

1. Clone the repository
2. Open MySQL Workbench
3. Run the SQL script in the following order:

   * Database & table creation
   * Data insertion
   * Analysis queries
4. View query outputs for insights

---

## 📁 Repository Structure

```
Airbnb-SQL-Analysis/
│── README.md
│── schema.sql
│── data_insert.sql
│── analysis_queries.sql
```

---

## 🎯 Learning Outcomes

* Advanced SQL querying (JOINs, CTEs, aggregations)
* Database design and normalization
* Business-focused data analysis
* Analytical thinking using relational data

---

## 📌 Use Cases

* Academic projects
* Internship submissions
* SQL portfolio projects
* Interview preparation

---

## 👩‍💻 Author

**Neha Pokale**
Aspiring Data Analyst | SQL | Power BI | Data Visualization

---

⭐ If you find this project useful, feel free to star the repository!
