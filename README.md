-- Problem: 175. Combine Two Tables
-- Goal: Retrieve first name, last name, city, and state
--       for each person from Person table.
--       If a person does not have an address,
--       city and state should return NULL.

SELECT 
    P.firstName,      -- Person's first name
    P.lastName,       -- Person's last name
    A.city,           -- City from Address table (may be NULL)
    A.state           -- State from Address table (may be NULL)
FROM Person P
LEFT JOIN Address A
    ON P.personId = A.personId;   -- Join condition based on personId
