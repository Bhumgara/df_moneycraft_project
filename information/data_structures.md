# Data Structure
This file stores information about how the data was presented, such that you can create your own test data to mimic the conditions of the data itself.

## Files
### moneycraft_accounts.csv 
One row per customer per active month. An account has closed (churned) when its rows stop — there is no churn column.

### moneycraft_marketing_spend.csv
One row per month per channel: what we spent winning customers.

### moneycraft_closure_reasons.csv
Recorded reasons for closed accounts — but only for some of them. This table is deliberately incomplete: many closures have no reason recorded.

## Data Fields
### Accounts
| Column | What it means |
| -------- | ------- |
| customer_id | Unique customer identifier. |
| month | Calendar month, e.g. 2023-04. |
| acquisition_channel | How the customer was won: Branch, Online, Comparison Site, Outbound, Referral or Broker/IFA. |
| region | UK region of the customer. |
| age_band | Customer age group. |
| account_tier | Packaged tier that month: Classic (£0), Silver (£11), Gold (£18) or Platinum (£28). Can change over time. |
| monthly_fee | Fee charged that month (£). Zero on Classic, or while a fee-waiver promo is running. |
| joined_on_promo | True if the customer joined on a 6-month fee-waiver promotion. |

### Marketing Spend
| Column | What it means |
| -------- | ------- |
| month | Calendar month. |
| channel | Acquisition channel (matches acquisition_channel above). |
| spend_gbp | Marketing spend in that channel that month (£). |

### Closure Reasons
| Column | What it means |
| -------- | ------- |
| customer_id | The customer who closed their account. |
| close_month | Month the account was closed. |
| reason_code | Recorded reason: Fees too high, Switched provider, Poor service, Unhappy with perks, Moved abroad, Bereavement or Unknown. |

## Data Formats
### Accounts
| Column | Example |
| -------- | ------- |
| customer_id | 1 |
| month | 2023-04 |
| acquisition_channel | Branch |
| region | London |
| age_band | 45-54 |
| account_tier | Gold |
| monthly_fee | 18 |
| joined_on_promo | FALSE |

### Marketing Spend
| Column | Example |
| -------- | ------- |
| month | 2024-11 |
| channel | Branch |
| spend_gbp | 17139.0 |

### Closure Reasons
| Column | Example |
| -------- | ------- |
| customer_id | 10755 |
| close_month | 2022-06 |
| reason_code | Fees too high |