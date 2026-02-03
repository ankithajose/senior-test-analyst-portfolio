1. Record Count Validation:
-- Source system
SELECT COUNT(*) 
FROM legacy_customer;

-- Target CRM
SELECT COUNT(*) 
FROM crm_customer;
Expected result : Counts should match (or align with migration scope).

2. Parent–Child Relationship Validation (JOIN)
SELECT c.customer_id, a.account_id
FROM crm_customer c
LEFT JOIN crm_account a
ON c.account_id = a.account_id
WHERE a.account_id IS NULL;

Expected result: 0 rows
Rows returned = orphan records (defect)

3. Invalid Email Detection (Post-Migration)
SELECT customer_id, email
FROM crm_customer
WHERE email NOT LIKE '%_@_%._%';
Output:Used to identify invalid emails accepted during migration

4. Duplicate Record Detection

SELECT email, COUNT(*)
FROM crm_customer
GROUP BY email
HAVING COUNT(*) > 1;
 Output: Detects duplicate customer records
 
