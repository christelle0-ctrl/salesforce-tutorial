# Salesforce tutorial

## Project description
This tutorial shows how to automate prospect and membership management
in Salesforce using Flow Builder. It contains three flows.

## 1. Prospect onboarding
When a new Lead is created, a decision (Lead Source Check) sends it down one of these paths:
- Website: a decision checks if a free trial was requested. If yes, a "Schedule Trial" task is created, otherwise a "Send Brochure" task. Both paths then create a "Sales Follow-up" task.
- Referral: creates a "Call Referrer" task, then a decision (Prospect Priority Check) creates a "Priority Call" task for hot leads or a "Welcome Offer" task for standard leads.
- Trade Show: creates a "Trade Show Offer" task and a "Newsletter" task.
- Other sources: no action.

## 2. Membership Subscription
A record-triggered flow that runs when an Opportunity is created.
A decision (Membership Type Check) sends the record down one of
three paths:
- Premium: creates a welcome task and updates the description
- Standard: creates a welcome task and an onboarding task
- Student: creates a check task and a discount task
- Other type: no action

## 3. Membership Renewal Reminder
A schedule-triggered flow that runs every day on Opportunities that
have a Membership end date. It calculates the days left before the
membership ends, then a decision (Time Left Check) chooses the path:
- Urgent (7 days or less): creates a call task and a discount task,
  then sends a renewal email if the contact has an email address
- Reminder (8 to 30 days): creates a renewal reminder task and a
  satisfaction check task
- Not Yet (more than 30 days): no action

## Custom field
- Opportunity: Membership end date (Date)

## Files
The screenshots in this repository show each flow.

## Video
Link coming soon
