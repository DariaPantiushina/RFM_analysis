# RFM analysis of the pharmacy chain's customer base

**Business context**: Pharmacy revenue typically declines during the off-season. The company has an SMS messaging system and wants to use it more effectively. To ensure the budget is spent wisely, the company plans to send personalized messages to customers.

**The purpose of this analysis** is to recommend ways to improve the effectiveness of SMS messaging.

**Objectives**:
1. To analyze the pharmacy chain’s customer base using RFM methodology, enabling classification of customers according to purchase behavior.
2. To provide targeted recommendations on product and service offerings for each customer segment.

## Data

1) bonuscheques(datetime, shop, card, bonus_earned, bonus_spent, summ, summ_with_disc, doc_id) - this table contains records of transactions made with bonus cards, which are linked to regular customers who provided their phone numbers.

"datetime" - date and time of the transaction;
"summ" - transaction (check) amount.

If a transaction was processed while the cash register was offline, the system recorded an encrypted sequence of characters instead of the actual card number. Since such records cannot be linked to specific customers, they were excluded from the analysis.

Additionally, customers who made only a single purchase were excluded. Since personalized discounts are intended to encourage repeat purchases and increase the average transaction value, offering them to one-time customers would not be meaningful.

2) Period covered by the analysis: July 2021 - June 2022.

The selected timeframe enables a reliable retrospective analysis and helps ensure that marketing efforts are not directed at customers who may no longer be reachable due to:

- relocation,

- a change in workplace that reduces the likelihood of visiting the pharmacy, or

- updated contact information (e.g., a new phone number)

