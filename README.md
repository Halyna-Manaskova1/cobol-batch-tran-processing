# COBOL Batch Transaction Processing

## Overview
This COBOL batch program evaluates card transactions against a
Merchant Category Code (MCC) reference table and assigns a risk code
to each transaction.

The result is written to an output file containing the original
transaction data enriched with risk information and a found/not-found status.

## Input Files
- **MCC-IN** – MCC to risk mapping (sequential)
- **TRAN-IN** – Card transactions (sequential)

## Output File
- **RISK-OUT** – Transactions enriched with risk information

## Processing Logic
- Load MCC data into an OCCURS table
- Read transactions sequentially
- Lookup MCC and determine risk
- Write output record
