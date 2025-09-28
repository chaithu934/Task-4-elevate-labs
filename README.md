1. Foundational Querying (SELECT, WHERE, ORDER BY, GROUP BY)
These are the building blocks of SQL, allowing you to select, filter, and organize data.

SELECT: The initial command to retrieve data. You used this to specify exactly which columns (Name, Sales, Genre) you needed for your analysis.

WHERE: Used to apply row-level filtering. You successfully used this to filter your data based on specific criteria (e.g., WHERE Sales > 20 or WHERE Genre = 'Action').

ORDER BY: Used to sort the result set. You used this to rank games by sales (ORDER BY Sales DESC), which is critical for identifying top performers.

GROUP BY: Used to aggregate identical data into groups. You used this to group your games by categories like Publisher or Genre before calculating summaries.

2. Analytical Functions (Aggregate Functions: SUM, AVG)
These functions transform detailed row data into meaningful summary statistics, which is the heart of business intelligence.

SUM: You used this to calculate the Total Sales for categories (like a specific Publisher or Genre), providing a measure of overall success.

AVG: You used this to determine the Average Sales per game for a Publisher or Genre, giving you a key benchmark figure that smooths out anomalies.

Combination: By using SUM(Sales) and COUNT(Name) along with GROUP BY Publisher, you created true performance metrics for your gaming data.

3. Advanced Query Logic (Subqueries and JOINS)
These techniques allow you to answer complex questions that require multiple steps of data retrieval and comparison.

Subqueries: You mastered nesting one query inside another.

Purpose: You used a subquery in the WHERE clause to compare individual game sales against a calculated global metric (e.g., finding games above the global average sales). This demonstrates contextual filtering.

Derived Tables: Using subqueries in the FROM clause allowed you to calculate complex aggregates (like average sales per publisher) and then join those results back to the original game data for a direct comparison.

JOINS (Self-Joins): While you had a single table, you successfully demonstrated the syntax and logic of INNER, LEFT, and RIGHT joins by performing a Self-Join.

Concept: This shows you can identify and compare relationships within the data (e.g., finding other games released by the same publisher), a necessary skill for working with multi-table databases.

4. Structure and Efficiency (Views and Indexes)
These final steps turn raw queries into reusable, efficient, and scalable database components.

Creating Views for Analysis:

Purpose: You created virtual tables (like Publisher_Summary). This abstracts complex grouping logic into a simple SELECT * FROM ViewName command. This is essential for reporting, consistency, and maintaining clean code.

Benefit: Analysts can query the summary view without needing to know the complex GROUP BY and aggregate functions that created it.

Optimizing Queries with Indexes:

Purpose: You created indexes on heavily used columns (Publisher, Genre, Sales). This is a critical step for performance.

Benefit: When your games_data table eventually grows to millions of rows, queries that filter or sort by these indexed columns will run hundreds of times faster, saving time and server resources.
