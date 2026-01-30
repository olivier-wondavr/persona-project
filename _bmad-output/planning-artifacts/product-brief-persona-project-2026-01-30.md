---
stepsCompleted: [1, 2, 3]
inputDocuments: []
date: 2026-01-30
author: ASUS
---

# Product Brief: persona-project

## Executive Summary

**persona-project** is an internal real-time analytics dashboard that unifies fragmented business metrics across Notion, Attio, and our internal CRUD system into a single, secure platform. Built for a team managing two products, it provides company-wide trend visibility for OKR meetings and client-specific insights for QBR preparation, enabling data-driven decisions without the security risks of external BI tools.

The platform addresses the critical pain point of manual CSV exports and unreliable Zapier integrations by building direct API connections to our data sources, delivering real-time insights accessible via Google SSO. Unlike generic BI tools, persona-project provides custom intelligence including automated simulation topic analysis, cross-product usage patterns, and power user identification - insights that off-the-shelf solutions cannot deliver.

---

## Core Vision

### Problem Statement

Our company currently uses three disconnected systems - Notion (tasks & bugs), Attio (clients & leads), and an internal CRUD (content created & analytics) - making it impossible to get a unified view of critical business metrics. Teams waste valuable time before OKR meetings manually exporting CSVs and importing them into Google Sheets, creating clunky, point-in-time snapshots that become outdated immediately. This fragmentation prevents leadership from seeing the full picture and blocks sales teams from preparing effectively for client QBRs with comprehensive usage data.

### Problem Impact

**Time & Efficiency:** Manual data aggregation before each strategic meeting drains productivity and delays decision-making. The CSV export workflow is brittle, time-consuming, and requires constant maintenance.

**Strategic Blindness:** Without real-time visibility across platforms, leadership cannot identify trends, spot issues early, or make informed decisions during OKR reviews. The growing complexity of managing two products with a small team makes this visibility even more critical.

**Sales Enablement Gap:** Sales teams lack the client-specific insights needed for compelling QBR conversations, unable to quickly access usage patterns, power users, or engagement trends for individual clients.

**Security & Compliance:** Current attempts to use Zapier introduce errors and potential security vulnerabilities. Sending sensitive client data through third-party integration platforms conflicts with our security-first approach.

### Why Existing Solutions Fall Short

**Generic BI Tools (Tableau, Metabase, Grafana):** Cannot understand our unique data model or provide the custom insights we need (simulation topic analysis, cross-product usage patterns). They also require sending sensitive data to external platforms, violating our security requirements.

**Integration Platforms (Zapier):** Prove unreliable with frequent errors, cannot handle the complexity of our data transformations, and introduce security risks by routing private client data through third-party services.

**Manual Google Sheets:** Current workaround is unsustainable - time-intensive, error-prone, and provides only static snapshots instead of real-time intelligence. Doesn't scale as the team and product portfolio grow.

### Proposed Solution

**persona-project** is a custom-built, real-time analytics dashboard that consolidates metrics from Notion, Attio, and our internal CRUD into a single, secure platform accessible via Google SSO. The solution features:

**Dual-Purpose Views:**
- **Company-Wide Dashboard:** Real-time metrics for OKR meetings showing tasks, bugs, client counts (paid/trial), AI simulations created, and cross-product usage trends
- **Client-Specific View:** Detailed client analytics for QBR preparation including usage patterns, power user identification, and engagement trends

**Intelligent Analytics:**
- Automated simulation topic analysis to understand what clients are building without manual exploration
- Usage trend detection identifying peak activity periods and behavioral patterns
- Power user identification across both product platforms
- Cross-product adoption and engagement metrics

**Technical Architecture:**
- Direct API integration with internal CRUD (endpoints to be built by dev team)
- Real-time data synchronization (minimum daily refresh, designed for real-time)
- Google SSO authentication ensuring company-only access
- Self-hosted solution keeping all data private and secure

### Key Differentiators

**Security-First Architecture:** Unlike SaaS BI tools, all data remains private within our infrastructure. No third-party services, no external data exposure, complete control over sensitive client information.

**Custom Intelligence:** Purpose-built analytics that generic tools cannot provide - simulation topic analysis, cross-product usage correlation, and behavioral insights specific to our two-product ecosystem.

**Owned Data Pipeline:** Building our internal CRUD API gives us complete control over data models, custom metrics, and exactly the aggregations we need without forcing our data into someone else's schema.

**Strategic + Sales Enablement:** Uniquely serves both executive strategy (OKR) and sales execution (QBR) needs in one platform, eliminating tool sprawl and ensuring everyone works from the same truth.

**Launch Timing Advantage:** With a new product just launched and growing complexity, building this infrastructure now establishes the foundation for scaling both products efficiently with a small team.

**Technical Team Ownership:** Having a dev team to build and maintain the solution eliminates dependence on external vendors, allows rapid iteration based on business needs, and ensures long-term sustainability.

---

## Target Users

### Primary Users

**Marketing Team Member - "Maya"**
- **Context:** Part of a small marketing team (2-3 people) managing client relationships and preparing QBRs for two products. Non-technical background.
- **Current Pain:** Depends on developers to export data from multiple systems. When she needs client stats before a call, she either waits for a developer to be available or works with outdated spreadsheets.
- **Goals:** Pull client-specific insights instantly before calls and QBRs. Identify success stories for case studies. Track client engagement trends.
- **Success Moment:** "I can pull any client's stats in under 30 seconds before a call - no more asking developers or scrambling with old spreadsheets."

**Product Team Member - "Paolo"**
- **Context:** Part of a small product team (2-3 people) managing two products. Non-technical, focused on product decisions and roadmap.
- **Current Pain:** Has no visibility into which features are actually being used, which clients are power users, or what types of simulations people are creating. Makes product decisions based on gut feel rather than data.
- **Goals:** See feature adoption at a glance. Identify power users vs. clients at risk of churning. Understand what simulations people are building to guide product direction.
- **Success Moment:** "I can see exactly which features are getting traction and spot at-risk clients before they churn - data I never had access to before."

### Secondary Users

**Developers (Indirect)**
- Build and maintain the dashboard and internal CRUD API endpoints
- No longer responsible for manual data exports once dashboard is live
- May access for troubleshooting or verifying data accuracy

### User Journey

- **Discovery:** Internal announcement to team - "here's your new dashboard"
- **Onboarding:** One-click Google SSO, immediate access to company data
- **Core Usage:** Monday morning check-ins as part of weekly rhythm; quick lookups before client calls or meetings
- **Success Moment:** First time pulling client stats in seconds instead of requesting an export
- **Long-term:** Becomes the single source of truth for OKR reviews and QBR preparation - no more spreadsheets

---
