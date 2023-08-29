# Introduction

Natural gas is a kind of clean energy, and liquefied natural gas (LNG) is the most popular form of its transportation. BoYuan is a fictional LNG logistics company in charge of LNG tankers shuttling back and forth in the Bohai Bay, an economically active sea area connecting many provinces and cities (Shandong, Liaoning, Hebei, and Tianjin) in China. However, the Yantai-Dalian route is accident-prone because it crosses busy container routes and connects several fishing grounds. Therefore, it will be a disaster if any accidents happen to an LNG tanker, such as LNG leakage or disposal.

The LNG logistics must be equipped with some safeguards measures, mainly represented as various emergency plans (aka business processes). An emergency plan cannot cover all possible situations. Taking BoYuan's case as an example, the execution of emergency response depends on many factors, including location of leak, amount of leak, state of tanker, ships nearby, and weather, etc., resulting in a significant number of factor combinations. A specific variant seldom happens. Due to cost constraints, making plans for all these combinations in advance is impossible. Once a particular accident happens, it needs an immediate response.

All responses must comply with a series of regulations assigned by authorities. The regulations are expressed as the following constraints.

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
