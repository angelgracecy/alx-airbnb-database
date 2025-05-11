🧩 Database Normalization to 3NF
✅ Objective
To ensure that the database schema is normalized up to the Third Normal Form (3NF) by removing redundancies and ensuring proper dependencies between attributes.

📊 1NF: First Normal Form
A table is in 1NF if:

All columns contain atomic (indivisible) values.

Each column contains values of a single type.

Each record is unique.

✅ Our schema meets 1NF:

Each attribute (e.g., email, name, price_per_night) holds atomic values.

No repeated groups or arrays are stored within a single field.

📊 2NF: Second Normal Form
A table is in 2NF if:

It is in 1NF.

All non-key attributes are fully functionally dependent on the primary key.

✅ Our schema meets 2NF:

Composite keys are not used, so full functional dependency is ensured.

For example, in the Booking table, all non-key attributes (like start_date, total_price) depend entirely on the primary key id.

📊 3NF: Third Normal Form
A table is in 3NF if:

It is in 2NF.

It contains no transitive dependencies (i.e., non-key attributes do not depend on other non-key attributes).

✅ Schema meets 3NF after review:

Table	Potential Issue	Resolution
User	No issues	Already normalized
Property	No issue, host_id is a FK, all other fields depend only on id	—
Booking	No transitive dependencies	—
Review	No transitive dependencies	—
Payment	All fields depend only on booking_id, which is the FK and primary reference	—

🛠 Summary of Normalization Steps
Ensured all values are atomic.

Separated concerns into distinct tables (e.g., Reviews in their own table instead of being nested in Properties).

Used foreign keys to represent relationships instead of duplicating data.

Ensured no field in a table is dependent on a non-primary attribute.

✅ Conclusion:
The Airbnb Clone database schema has been successfully normalized to Third Normal Form (3NF) to optimize data integrity and reduce redundancy.









