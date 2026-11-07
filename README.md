# FitLife: automating a gym with Salesforce

Our project is about a fictional gym called FitLife. We used Salesforce
to automate part of its daily work.

## What is Salesforce?
Salesforce is an online program that companies use to keep all their
customer information in one place (a CRM). Think of it as a big
notebook that every employee can open, but on the computer.
There is nothing to install: you request a free Developer Edition account here (it stays available as long as you keep using it):
https://developer.salesforce.com/signup


## Why we built this
At a gym, employees have to contact new prospects quickly, welcome each
new member depending on their plan, and remind members before their
membership ends. They are busy, so some of these steps get forgotten.
We built 3 flows (automations) to do it for them.

## Words to know
- Lead: someone who might want to join
- Opportunity: a possible sale, here a membership
- Task: something an employee has to do
- Flow: a Salesforce tool that does this automatically, without code

Each flow works the same way: a trigger (when it starts), a decision
(which path to take), and an action (usually creating a task).

## Our 3 flows
1. **Prospect Onboarding**: starts when a Lead is created. It checks
   where the person comes from (website, referral, trade show) and
   creates different tasks for the employee.
2. **Membership Subscription**: starts when an Opportunity is created
   or updated. It checks the plan (Premium, Standard, Student) and
   creates the right welcome tasks.
3. **Membership Renewal Reminder**: runs every day. It checks how many
   days are left before a membership ends. If it is 7 days or less, it
   creates tasks and sends an email. If it is 30 days or less, it
   creates lighter reminder tasks.

## Videos
- Flow 2, Membership Subscription: [Workflow 2.mov]
- Flow 3, Membership Renewal Reminder: [Workflow 3.mov]

Screenshots of each flow are also in this repository.

## What we would improve
Flow 2 can run again at every update, and Flow 3 can send the same
reminder several days in a row. In a real company, we would add a
condition or a field to avoid that.
