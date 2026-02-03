Data Integrity Checks – CRM Data Migration
This document outlines the data integrity validation checks performed during CRM data migration testing. These checks ensure that migrated data remains accurate, complete, and consistent, and that business-critical relationships are preserved.

Record Count & Completeness
Validate total record counts between source and target systems match
Validate no unexpected data loss during migration
Validate all mandatory fields are populated in the target system

Referential Integrity

Validate parent–child relationships are preserved
Validate child records do not exist without a valid parent
Validate relationship IDs are correctly mapped
Validate many-to-many relationships remain intact

Data Accuracy & Consistency

Validate field values in the target system match the source
Validate transformed fields follow defined business rules
Validate date formats and time zones are consistent
Validate numeric fields retain precision and scale

Duplicate & Invalid Data

Validate duplicate customer or contact records are not created
Validate duplicate detection rules function post-migration
Validate invalid data (e.g. malformed emails) is handled or flagged appropriately

Post-Migration Behaviour

Validate migrated records can be edited and saved without errors
Validate workflows and automation trigger correctly on migrated data
Validate reporting and search functions work using migrated records

Risk-Based Focus

Integrity checks prioritised:
Customer master data
Financial or revenue-impacting records
Compliance-sensitive fields
High-usage business workflows

Outcome:
These checks help identify data quality risks early and ensure migrated data supports real business operations.
