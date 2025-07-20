---
layout: default
title: Home
nav_order: 1
description: "Reporting System Documentation"
permalink: /
has_children: true
---

# Reporting System Model Creation Guide

Welcome to the comprehensive guide for creating model instances in your bush regeneration application. This documentation is organised by model dependencies to ensure you create models in the correct order.

## Quick Start

1. **[Understanding Dependencies](getting-started/understanding-dependencies)** - Learn about model relationships
2. **[Navigation Overview](getting-started/navigation-overview)** - Familiarize yourself with the admin interface
3. **[Foundation Models](foundation-models/)** - Start with independent models
4. **[Core Models](core-models/)** - Build on foundation models
5. **[Business Models](business-models/)** - Implement main functionality
6. **[Feature Models](feature-models/)** - Add advanced features

## Model Categories

### 🔵 Foundation Models
These models have no dependencies and should be created first:
- **Weeds & Natives**: Flora species definitions
- **Tool Types**: Equipment and tool categories  
- **Work Categories**: Types of work activities
- **Organization Types**: Client organization classifications
- **Pay Scale**: Hourly rates and compensation
- **Roles**: User permission groups
- **Marker Types**: Map marker classifications

### 🟣 Core Models  
These depend on Foundation models:
- **Users**: System users (staff) with roles and pay scales
- **Contacts**: People associated with organizations
- **Organizations**: Client companies and entities
- **Weather Stations**: Weather stations for spray reports
- **Base Boundaries**: Geographic area definitions
- **Base Markers**: Map location points
- **Zones**: Operational area divisions

### 🟠 Business Logic Models
These implement main business functionality:
- **Worksites**: Job locations (depend on boundaries, markers, zones)
- **Purchase Orders**: Equipment and supply requests
- **Site Reports**: Work completion documentation
- **Worksite Boundaries**: Specific work area definitions

### 🟢 Feature Models
Advanced features that depend on all previous layers:
- **Rosters**: Staff scheduling and assignments
- **Incidents**: Safety and issue reporting  
- **Detailed Reports**: Comprehensive work documentation
- **Hours Worked**: Time tracking and payroll

## Model Creation Order

{: .label .label-green }
Recommended Order

Create models in this sequence to avoid dependency errors:
```mermaid
graph TD
    A[Foundation Models] --> B[Core Models]    
    B --> C[Business Logic Models] 
    C --> D[Feature Models]
    
    %% Foundation Models (no dependencies)
    A1[Weeds] --> A
    A2[Natives] --> A
    A3[Tool Types] --> A
    A4[Work Categories] --> A
    A5[Organization Types] --> A
    A6[Pay Scale] --> A
    A7[Roles] --> A
    A8[Marker Types] --> A
    
    %% Core Models (depend on Foundation)
    B1[Users] --> B
    B2[Contacts] --> B
    B3[Organizations] --> B
    B4[Weather Stations] --> B
    B5[Base Boundaries] --> B
    B6[Base Markers] --> B
    B7[Zones] --> B
    
    %% Business Logic Models (depend on Core + Foundation)
    C1[Worksites] --> C
    C2[Purchase Orders] --> C
    C3[Site Reports] --> C
    C4[Worksite Boundaries] --> C
    
    %% Feature Models (depend on all previous layers)
    D1[Rosters] --> D
    D2[Incidents] --> D
    D3[Detailed Reports] --> D
    D4[Hours Worked] --> D
    
    %% Key Dependencies (shown as dotted lines)
    A6 -.-> B1
    A7 -.-> B1
    A8 -.-> B6
    B1 -.-> C1
    B5 -.-> C4
    B6 -.-> C1
    B7 -.-> C1
    A4 -.-> C1
    C1 -.-> D1
    C1 -.-> D3
    B1 -.-> D1
    B1 -.-> D4
    
    %% Styling
    classDef foundation fill:#e1f5fe
    classDef core fill:#f3e5f5
    classDef business fill:#fff3e0
    classDef feature fill:#e8f5e8
    
    class A1,A2,A3,A4,A5,A6,A7,A8 foundation
    class B1,B2,B3,B4,B5,B6,B7 core
    class C1,C2,C3,C4 business
    class D1,D2,D3,D4 feature
```
---

## Getting Started

Begin with [Understanding Dependencies](getting-started/understanding-dependencies) to learn about model relationships, then proceed through the categories in order.