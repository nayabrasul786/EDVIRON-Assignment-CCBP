# EDVIRON-Assignment-CCBP
# Data Analyst – Excel / Power BI Assignment

# EDVIRON Revenue, Commission & Settlement Analytics

# Data Analyst Assignment – Excel Modeling & Dashboard

# Prepared by: Shaik Nayab Rasul
# Date: March 2026

Project Overview

This project analyzes transactional payment data processed through Edviron’s platform. The objective is to clean raw financial data, normalize pricing structures, compute revenue splits across ERP partners and Edviron, and build an interactive dashboard for revenue and settlement analytics.

The solution was implemented using Microsoft Excel, incorporating structured modeling, financial logic computation, PivotTables, and dashboard visualization.

# File Structure

The Excel solution file contains the following sheets:

1. Raw_Data

Contains the original imported dataset without modification.

Purpose:

Maintain auditability

Ensure original data remains unchanged

2. Clean_Data

Contains cleaned and standardized version of raw data.

Cleaning performed:

Removed formatting inconsistencies

Standardized pricing type (FLAT / PERCENT)

Ensured numeric consistency

Flagged missing or inconsistent values

3. Calc_Model

This is the core financial computation layer.

It converts pricing into INR values and calculates revenue metrics per transaction.

Computed Columns:

Partner_Pricing_INR
Merchant_Pricing_INR
Edviron_Buying_INR

ERP_Revenue
= Merchant Pricing − Partner Pricing

Edviron_Net_Revenue
= Partner Pricing − Edviron Buying

Edviron_Gross_Revenue
= ERP Revenue + Edviron Net Revenue

Settlement Fields:

ERP_Payable
Edviron_Retained
Pending_Exposure

Exception_Flag
Flags negative margin or pricing errors.

4. Reports

Contains PivotTables for analytical reporting:

Revenue Summary
Partner Performance
Gateway Analysis
Payment Method Analysis
Exposure Report

5. Dashboard

Interactive dashboard displaying key metrics and charts.

Key Metrics:

Total Transactions
Total GMV
ERP Revenue
Edviron Net Revenue
Edviron Gross Revenue
Pending Exposure
Unique Users

Charts:

Revenue split
Time-based revenue trend
Gateway contribution
Payment method mix

Filters:

Date filter
Partner filter
Gateway filter
Payment method filter

Dashboard updates dynamically using PivotTables and slicers.

6. Assumptions_Notes

Contains financial assumptions and modeling logic.

Key assumptions include:

Percentage pricing is applied on Transaction Amount.

Settlement logic:

SUCCESS → Settled
PENDING → Exposure
FAILED → Ignored in settlement

ERP Payable equals ERP Revenue.
Edviron Retained equals Edviron Net Revenue.

Revenue Logic Explanation

There are three pricing layers:

Edviron Buying Price → Cost to Edviron
Partner Pricing → Price Edviron charges ERP
Merchant Pricing → Price ERP charges school

Revenue formulas:

ERP Revenue
= Merchant Pricing − Partner Pricing

Edviron Net Revenue
= Partner Pricing − Edviron Buying

Edviron Gross Revenue
= ERP Revenue + Edviron Net Revenue

Settlement Logic

Payment gateway settles full amount to Edviron.

Edviron then settles ERP share.

Settlement classification:

SUCCESS → Fully settled

PENDING → Exposure exists

FAILED → No settlement

Exposure includes:

ERP payable outstanding
Edviron receivable risk

Dashboard Features

Interactive filtering
Dynamic KPI updates
Automated revenue calculations
Pivot-driven reporting
Exception detection

Exception Handling

Exception flags identify:

Negative margin transactions
Missing pricing
Settlement inconsistencies

This ensures financial accuracy and auditability.

Tools Used

Microsoft Excel
Power Query
PivotTables
PivotCharts
Excel Formulas
Structured Data Modeling

How to Use

Step 1: Paste dataset into Raw_Data sheet

Step 2: Copy into Calc_Model sheet

Step 3: Drag formulas down

Step 4: Refresh PivotTables

Step 5: View Dashboard

Key Business Insights Enabled

Revenue performance tracking

Partner profitability analysis

Payment gateway contribution analysis

Settlement exposure monitoring

Financial reconciliation support

Conclusion

This solution provides a structured, scalable, and audit-ready analytics model for revenue and settlement tracking.

It demonstrates strong capabilities in:

Data cleaning
Financial modeling
Excel analytics
Dashboard development
Business analysis
