# Kanyisa Reference System
## Official Definitions and Conventions

Version: 1.0

---

# 1. Purpose

The Republic of Kanyisa is a fictional country developed as the reference system for the Kanyisa Energy Modelling Toolkit.

Kanyisa is intentionally designed to resemble South Africa while remaining independent of any real-world institution, policy document, modelling study, or dataset. The objective is to provide a realistic yet reusable environment for energy systems modelling, capacity expansion planning, and OSeMOSYS training.

This document serves as the authoritative source for terminology, institutions, geography, planning assumptions, and modelling conventions used throughout the toolkit.

All project documentation shall conform to the definitions provided herein.

---

# 2. Design Principles

The Kanyisa Reference System shall be:

1. Realistic enough to resemble a modern Southern African power system.
2. Generic enough to be adapted for other national contexts.
3. Simple enough for learning and training purposes.
4. Detailed enough for policy and planning analysis.
5. Consistent across all project documentation.

When realism and simplicity conflict, simplicity should generally be preferred.

---

# 3. Country Identity

| Attribute | Value |
|------------|------------|
| Official Name | Republic of Kanyisa |
| Short Name | Kanyisa |
| Adjective | Kanyisan |
| Capital City | Lumina |
| Currency | Kanyisa Rand (KZR) |
| Time Zone | UTC+2 |
| Region | Southern Africa |
| Government Type | Constitutional Republic |
| Motto | Powering Prosperity Sustainably |

---

# 4. Geography

## National Context

Kanyisa occupies the southernmost portion of the African continent and possesses extensive coastlines, significant mineral resources, and diverse renewable energy potential.

## Geographic Zones

| Region | Characteristics |
|----------|----------|
| Western Region | High solar resource, semi-arid climate |
| Coastal South | Strong wind resource |
| Central Plateau | Industrial and economic heartland |
| Northern Basin | Mining-intensive region |
| Eastern Highlands | Agriculture and hydro resources |

---

# 5. Population and Economy

## Population

| Year | Population |
|----------|----------|
| 2025 | 63 million |
| 2030 | 67 million |
| 2040 | 75 million |
| 2050 | 82 million |

## Economic Structure

Major sectors include:

- Mining
- Manufacturing
- Financial Services
- Agriculture
- Transport
- Tourism

### Energy-Intensive Industries

- Precious Metals Mining
- Ferroalloys
- Steel Production
- Chemicals
- Cement Manufacturing

Electricity demand is strongly influenced by industrial and mining activity.

---

# 6. Government Institutions

## Ministry of Energy and Minerals (MEM)

Responsible for:

- National energy policy
- Integrated energy planning
- Resource development
- Energy security

---

## Energy Regulation Authority (ERA)

Responsible for:

- Licensing
- Tariff regulation
- Market oversight
- Compliance enforcement

---

## National Planning Commission (NPC)

Responsible for:

- Long-term development planning
- Infrastructure coordination
- National development strategy

---

# 7. Electricity Sector Institutions

## Kanyisa Power Corporation (KPC)

State-owned utility responsible for:

- Legacy generation assets
- Distribution operations
- Retail electricity supply

---

## Kanyisa Transmission Company (KTC)

Independent transmission system and market operator responsible for:

- Transmission planning
- Grid expansion
- System operation
- Market administration

---

## Independent Power Producers (IPPs)

Private entities participating in generation development and electricity supply through competitive procurement programmes or bilateral arrangements.

---

# 8. National Planning Framework

## National Electricity Plan (NEP)

Primary electricity planning document.

The NEP establishes:

- Capacity expansion pathways
- Resource adequacy requirements
- Reliability standards
- Emissions trajectories
- Technology deployment targets

---

## Integrated Energy Strategy (IES)

Long-term cross-sector energy planning framework.

---

## National Development Vision 2050 (NDV 2050)

National economic and infrastructure development strategy.

---

## Just Transition Framework (JTF)

Framework guiding the transition to a lower-carbon economy while supporting workers, communities, and economic development.

---

# 9. Electricity System Overview

## 2025 Baseline

| Metric | Value |
|------------|------------|
| Installed Capacity | ~60 GW |
| Peak Demand | ~35 GW |
| Annual Demand | ~220 TWh |
| Electrification Rate | >90% |
| Grid Coverage | National Interconnected System |

Kanyisa operates the largest interconnected electricity system on the African continent.

---

# 10. Technology Classification

The reference system includes the following technology groups.

## Thermal Generation

- Coal
- Open Cycle Gas Turbine (OCGT)
- Combined Cycle Gas Turbine (CCGT)
- Diesel Peaking Generation

## Renewable Generation

- Solar PV
- Wind
- Hydropower
- Biomass

## Storage

- Pumped Storage
- Battery Energy Storage Systems (BESS)

## Other

- Nuclear
- Electricity Imports
- Electricity Exports

Detailed technology definitions are maintained in `technology_catalogue.md`.

---

# 11. Resource Endowment

## Coal

Large domestic reserves support historically significant coal-fired generation capacity.

## Solar

Excellent solar irradiation across western and central regions.

## Wind

High-quality wind resources along coastal corridors.

## Gas

Limited domestic resources supplemented by regional and international imports.

## Hydro

Modest domestic potential with opportunities for regional imports.

---

# 12. Market Structure

The electricity sector consists of:

1. State-owned generation.
2. Independent power producers.
3. Municipal procurement.
4. Bilateral contracting.
5. Regional electricity trade.

The reference system assumes progressive market reform over time.

---

# 13. Regional Integration

## Southern African Energy Pool (SAEP)

Kanyisa participates in the Southern African Energy Pool.

Regional interconnections enable:

- Energy imports
- Energy exports
- Reserve sharing
- Regional optimisation
- Improved system flexibility

---

# 14. Reliability Standards

## Planning Reserve Margin

Default planning reserve margin:

**15%**

Sensitivity studies may evaluate:

- 10%
- 20%
- 25%

## Reliability Objective

Electricity demand shall be supplied while maintaining adequate operating reserves and long-term resource adequacy.

---

# 15. National Energy Objectives

The Republic of Kanyisa seeks to:

1. Maintain security of supply.
2. Eliminate sustained electricity shortages.
3. Support economic growth.
4. Expand electricity access.
5. Strengthen transmission infrastructure.
6. Increase renewable energy deployment.
7. Reduce greenhouse gas emissions.
8. Promote regional integration.
9. Enable a just and orderly energy transition.

---

# 16. Scenario Framework

The following scenario names are reserved throughout the toolkit.

## Reference Case

Continuation of current policies and plans.

## Least Cost Scenario

System development determined by cost optimisation.

## Low Carbon Scenario

Development subject to emissions constraints.

## High Demand Scenario

Accelerated economic and electricity demand growth.

## Delayed Transition Scenario

Reduced pace of decarbonisation and renewable deployment.

## Net Zero Scenario

Deep decarbonisation pathway consistent with long-term climate objectives.

---

# 17. Modelling Conventions

## Currency

All costs shall be reported in:

**KZR 2025 Real Terms**

Unless otherwise specified.

## Horizon

Default modelling horizon:

**2025–2050**

## Time Resolution

The default temporal structure shall be documented within individual model configurations.

## Reporting Units

| Metric | Unit |
|----------|----------|
| Capacity | MW |
| Energy | GWh or TWh |
| Cost | KZR |
| Emissions | tCO₂ |
| Fuel Consumption | PJ |

---

# 18. Document Hierarchy

This document is the highest-level reference within the Kanyisa Toolkit.

All other documents shall align with this reference system, including:

- country_profile.md
- geography.md
- institutions.md
- power_system.md
- demand.md
- transmission_system.md
- technology_catalogue.md
- energy_policies.md
- modelling_assumptions.md
- scenario_framework.md
- data_sources.md

Where inconsistencies occur, this document shall take precedence.

---