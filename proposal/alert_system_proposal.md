# Alert System Proposal

This proposal shows a system that send alerts to users based on spending patterns, leveraging the Monthly Pace metric defined in the analysis. The main goal is to provide actionable insights to help users manage their cash flow.

## The system would work as follow:

1. **Data Aggregation**: The system will continuously monitor user transactions (income and expenses).
2. **Metric Calculation - Monthly Pace**: The system will periodically (dailly or weekly) calculate the metric. It forecast the total monthly spending based on the average daily spending up to that point.
    - **Monthly Pace** = (Total Spent to Date / Current Day of Month) * (Total Days in Month)
3. **Threshold Comparison**: The calculated value for Monthly Pace would be compared against user-defined or system-suggested threshold. This value suggested by the system will be different for each client based on the financial data we have about them.
4. **Alert Trigger**: If a metric reaches a consumption percentage defined by the user or suggested by the system, the system activates the trigger to send the alert message. Similarly, when the total spending limit for the current month defined by the user or suggested by the system is reached, the alert system activates the trigger and sends the alert message.
5. **Notification**: The user can configure the notification method or accept a system suggestion. The notification can be scheduled (e.g., every day at 9 AM), whenever it reaches the defined threshold, or whenever it hits the user's spending limit. Then, the user receives an alert notification. (e.g., notification via e-mail, in-app, push notification on the fone)
6. **Context and Action**: The notification can be send with a link that enable the user to view a detailed analysis of their spendings and recent transactions, and suggest possible actions.

## Data Presented to the User

- Type of Alert: A notification that clearly state what kind of alert it is.
- Show the projected total monthly spending (e.g., "You have already spent R$ xyz this month. Your limit is R$ pto.")
- If the user access the full report, we can display a comparison between the current month and the past month. We can also display other types of information.
- Threshold Information: The system can metion the threshold that was crossed (e.g., "Alert triggered: Your spending is projected to exceed your limit for this month.")

## Configurable Parameter

1. **Threshold**: The user can define an absolute projected spending amount for the current month (e.g., alert if projected > R$ 3000). A percentage that, if reached out, trigger the alert (e.g., alert if projected >= 40%).
2. **Frequency / Timing**: The user can choose how often the metric is checked/updated. The user can choose if any alert will be triggered. The user can choose how often the notification will be sent by scheduling the frequency, or setting it to trigger whenever some threshold is reached.
3. **Reference Income/Budget**: The system allow the users to input their typical income or set a monthly budget. The user can accept a system suggested income/budget based on historical data.

## Example Alert Message:

#### Monthly Pace Alert (Triggered because projected spending exceeded 75% of the budget threshold defined by the user)

**Spending Pace Alert!**

Hi <name>. As of day 15/30 this month, your spending pace projects a total of R$ 3220.00 by the end of the month. This projection is 83% of your typical budget.
Would you like to view a datailed analysis of your recent transactions and historical comparisons?