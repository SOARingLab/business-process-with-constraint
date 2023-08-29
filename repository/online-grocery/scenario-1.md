# Introduction

A simplified online grocery chaining business, CAICAI, provides non-staple foods for residents in many cities in China. CAICAI takes the franchising business scheme where each franchisee shares a standard business process developed and provided by the franchiser. As usual, the franchiser enforces strict governance rules on the business process.

The business process runs smoothly until COVID-19 appeared. The rapidly changing epidemic prevention policy makes franchisees unable to operate normally. The franchiser cannot keep adjusting the business process as soon as possible to maintain the resilience of the business. What's worse, the epidemic situation and epidemic prevention policies are different in different regions. Thus, each franchisee tries to tailor business process customized to its situation accordingly.

To ensure that tailored businesses comply with business regulations, the franchiser specifies the following constraints.

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
