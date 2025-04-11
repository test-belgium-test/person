# Technical Notes – Personal Data Constraints (e-Test 3.0)

This document outlines key constraints and definitions for personal data types used within the e-Test 3.0 project.

## General Constraints

### Required Fields
The following fields must always be provided:
- **First Name** (`firstName`): String, non-empty.
- **Last Name** (`lastName`): String, non-empty.
- **Birthdate** (`birthDate`): Date formatted as `YYYY-MM-DD`.
- **Gender** (`gender`): Integer (0, 1, or 2) as per ISO 5218 standard.
- **Address** (`address`): Full address provided as a single string.

### Optional Fields
- **Phone Number** (`phoneNumber`): String, expected to be in international format (e.g., `+32 475 12 34 56`). Useful for contact and notification purposes.

## Specific Constraints and Standards

### GenderCode
Gender is represented according to the ISO 5218 standard:
- `0` – Unknown (gender cannot be determined or is not provided).
- `1` – Male
- `2` – Female

Code `9` (Not Applicable) from the ISO 5218 standard is explicitly excluded, as it is not relevant to the personal data context used here.

### HouseholdRelationTypeCode
This field represents the relationship of an individual to the reference person of a household. Constraints:
- Integer value between `1` and `99`.
- Codes are defined and maintained by the National Register. Ensure synchronization with the current National Register definitions.

### CivilStatusTypeCode
Represents the civil status of an individual (e.g., single, married, divorced).
- Integer value between `1` and `99`.
- Refer to the National Register for precise meaning and updates on each code.

## Date Format
- All dates must adhere strictly to the `YYYY-MM-DD` format to ensure consistency across all integrated systems.

## Address Field
- The address must include sufficient detail (street, number, postal code, city, country) for accurate identification and verification.
- Recommended to follow national or international address standards to facilitate integration and validation.

## Usage Recommendations
- Always validate JSON data against the provided Swagger/OpenAPI schema before integration.
- Ensure compliance with all specified minimum and maximum numeric constraints to avoid validation errors.

For further details or specific questions regarding constraints, consult the official e-Test 3.0 documentation or reach out to the project maintainers.
