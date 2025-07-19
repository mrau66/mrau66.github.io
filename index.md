---
layout: default
title: Home
nav_order: 1
description: "Django Model Creation Documentation"
permalink: /
has_children: true
---

# Django Model Creation Guide

Welcome to the comprehensive guide for creating model instances in your Django application. This documentation is organized by model dependencies to ensure you create models in the correct order.

## Quick Start

1. **[Understanding Dependencies](getting-started/understanding-dependencies)** - Learn about model relationships
2. **[Navigation Overview](getting-started/navigation-overview)** - Familiarize yourself with the admin interface
3. **[Foundation Models](foundation-models/)** - Start with independent models
4. **[Core Models](core-models/)** - Build on foundation models
5. **[Business Models](business-models/)** - Implement main functionality
6. **[Feature Models](feature-models/)** - Add advanced features

## Model Creation Order

{: .label .label-green }
Recommended Order

Create models in this sequence to avoid dependency errors:

```mermaid
graph TD
    A[Foundation Models] --> B[Core Models]
    B --> C[Business Models] 
    C --> D[Feature Models]
    
    A1[Weeds] --> A
    A2[Natives] --> A
    A3[Tool Types] --> A
    A4[Work Categories] --> A
    A5[Organization Types] --> A
    
    B1[Users] --> B
    B2[Organizations] --> B
    B3[Weather Stations] --> B
    
    C1[Worksites] --> C
    C2[Purchase Orders] --> C
    C3[Site Reports] --> C
    
    D1[Rosters] --> D
    D2[Incidents] --> D
    D3[Detailed Reports] --> D
```