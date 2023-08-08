# Introduction

The business process of an online grocery.

# Functional Constraint

* Once "Deliver goods" executes, "Process payment" should execute as well.

# Non-functional Constraint

* customer_satisfaction >= 8
* cost_indicator <= 12

## KPI

* customer_satisfaction = goods_quality + issue_priority - delivery_time / 20 + discount_amount / 10
* cost_indicator = goods_quality + issue_priority + discount_amount / 10

## Valuation

| Activity | Variable | Value | Type |
| ---- | ---- | ---- | ---- |
| Pick goods | goods_quality | \[3,5\] | uncontrollable |
| Issue goods | issue_priority | \[3,5\] | controllable |
| Confirm delivery | delivery_time | \[0,120\] | uncontrollable |
| Process payment | discount_amount | \[0,50\] | controllable |
