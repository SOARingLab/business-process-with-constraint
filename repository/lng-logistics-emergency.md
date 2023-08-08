# Introduction

The emergency response process of LNG logistics.

# Functional Constraint

* Before "Plug leak" executes, "Ventilate" should have executed, to reduce the gas concentration.
* Before "Put out fire" executes, "Close doors and block vents" should have executed, to cut off oxygen and control the fire area.
* Before "Eject goods" executes, "Change course" should have executed, to deviate from public waterways.
* Once "Change course" executes, "Contact relevant bureaus" should execute.

# Non-functional Constraint

* 20 <= resource_consumption <= 60
* safety_level >= 3

## KPI

* resource_consumption is the total resource consumption of all activities.
* safety_level is the average safety level of all activities.

## Valuation

| Activity | Variable | Value | Type |
| ---- | ---- | ---- | ---- |
| Disconnect pipes and leave dock | resource_consumption | \[3,5\] | uncontrollable |
| Change course | resource_consumption | \[5,10\] | uncontrollable |
| Contact relevant bureaus | resource_consumption | \[1,2\] | controllable |
| Check for danger | resource_consumption | \[2,5\] | controllable |
| Check for danger | safety_level | \[1,9\] | uncontrollable |
| Disperse gas | resource_consumption | \[5,10\] | uncontrollable |
| Disperse gas | safety_level | \[4,8\] | controllable |
| Put out fire | resource_consumption | \[10,25\] | uncontrollable |
| Put out fire | safety_level | \[2,8\] | controllable |
| Wear protective gears | safety_level | \[2,7\] | uncontrollable |
| Check goods condition | resource_consumption | \[1,7\] | controllable |
| Transfer goods | resource_consumption | \[5,10\] | uncontrollable |
| Eject goods | resource_consumption | \[10,15\] | uncontrollable |
