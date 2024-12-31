# Sprint 4 - Statistical Data Analysis

I work as an analyst for the telecommunications company Megaline. The company offers customers two prepaid plans: Surf and Ultimate. The sales department wants to know which of the plans generates more revenue to adjust the advertising budget.

You will perform a preliminary analysis of the plans based on a small selection of customers. You will have data from 500 Megaline customers: who the customers are, where they are from, which plan they use and the number of calls and messages made in 2018. My job is to analyze customer behavior and determine which prepaid plan generates more revenue. In this project, you will see exactly what aspects of customer behavior you need to analyze. Determining which plan, on average, generates more revenue is a task that can be solved using statistical tests. 

---

## Step 1. Open the data file and study the general information

## Step 2. Prepare the data

Convert the data to the required types.

Find and eliminate errors in the data. Be sure to explain which errors you found and how you eliminated them.

For each user, find:
- The number of calls made and minutes used per month
- The number of text messages sent per month
- The volume of data per month

- The monthly revenue generated from each user. To do this, you need to:
- Subtract the free package limit from the total number of calls, text messages and data;
- Multiply the result by the plan value;
- Add the monthly price depending on the plan.

## Step 3. Analyze the data

Describe customer behavior:

- Find the minutes, text messages and data volume that users of each plan need per month.
- Calculate the mean, variance and standard deviation.
- Build histograms. Describe the distributions.

## Step 4. Test the hypotheses

- The average revenues for Ultimate and Surf plan users are different.

- The average revenues for NY-NJ area users are different from those for users in other regions.

## Step 5. Final Conclusion

---
# Data Dictionary

The `users` table (data about users):

- `user_id` — unique identifier for the user
- `first_name` — first name for the user
- `last_name` — last name for the user
- `age` — age of the user (in years)
- `reg_date` — sign-up date (dd, mm, yy)
- `churn_date` — the date the user stopped using the service (if the value is missing, it means the plan was in use when the database was scraped)
- `city` — city where the user lives
- `plan` — name of the plan

The `calls` table (data about calls):

- `id` — unique identifier for the call
- `call_date` — date of the call
- `duration` — duration of the call (in minutes)
- `user_id` — identifier for the user making the call

The `messages` table (data about text messages):

- `id` — unique identifier for the text message
- `message_date` — date of the text message
- `user_id` — identifier for the user sending the text message

The `internet` table (data about web sessions):

- `id` — unique session identifier
- `mb_used` — amount of data used during the session (in megabytes)
- `session_date` — date of the web session
- `user_id` — user identifier

The `plans` table (plan data):

- `plan_name` — plan name
- `usd_monthly_fee` — monthly price in US dollars
- `minutes_included` — monthly package of minutes
- `messages_included` — monthly package of text messages
- `mb_per_month_included` — amount of data package (in megabytes)
- `usd_per_minute` — price per minute after exceeding the package limit (for example, if the package includes 100 minutes, the first minute in excess will be charged)
- `usd_per_message` — price per text message after exceeding the package limit
- `usd_per_gb` — price per extra gigabyte of data after exceeding the package limit (1 GB = 1,024 megabytes)
