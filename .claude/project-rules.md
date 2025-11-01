# Project Rules for SME-MLG Data Products

## 1. Schema Usage
- Use local schema only: "../ODPS4.1/schema/odps.json"
- No remote URLs
- Reject any field not defined in the schema

## 2. File Format
- YAML only
- One data product per file

## 4. Naming and IDs
- productID must be unique and match the file name theme
- No spaces in IDs

## 5. Validation
- Always reference the current ODPS version in the file
- Do not add fields unless confirmed in schema

## 6. Behavior Rules for Claude
- Do not infer business attributes
- Ask for clarification when information is missing
- If validation cannot be ensured, stop and request schema context

## 7. Change Control
- Any new field requires schema update before use

## 8. Minimal Data Product Definition
- When "minimal" or "minimum" is requested, include only basic product details:
  - Required schema fields only
  - NO pricing plan
  - NO SLA or data quality
  - No access component
  - No license terms
  - No Core support contact information
- Avoid extensive or elaborate content in descriptions
- Keep all text fields concise and to the point
- create only english version

Example:

schema: https://opendataproducts.org/v4.1/schema/odps.yaml
version: 4.1
product:
  en:
    name: Pets of the year
    productID: 123456are
    visibility: private
    status: draft
    type: derived data
