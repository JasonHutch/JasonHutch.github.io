---
title: Agentic Intranet Search
date: 2026-01-10 14:30:00 -0600
categories: [Portfolio,Work]
tags: [work project,Azure Foundry, Agent Framework, Copilot Studio]
---

## Project Description

Create a search overview SharePoint Framework webpart mimicking Google's search overview. This component sat above other search webparts on the client's intranet portal. This search overview had the capabilities to leverage caching, Copilot Studio agents, and a series of curated knowledge sources managed in SharePoint to ensure agent responses are accurate and arrive with low latency.

### Features
*   Define curated based answers and knowledge sources to influence agent responses.
* Orchestrator agent capable of fetching grounding information and building prompt to be sent downstream to agent responsible for responses.
* Redis cache used to cache agent responses and tool calls to ensure performance of searches

### Responsibilities

* Develop search API & Agentic architecture.
* Create & deploy .NET API to act as agent service for the intranet experience
* Build routing agent and tools using Microsoft Agent Framework instrumented with Azure Application insights to track metrics.
* Establish connection to Copilot Studio from API using Entra ID
* Provide estimates on token consumption and how various aspects of the workflow could impact month cost.

### Technology Used

* .NET
* Microsoft Agent Framework
* Azure AI Search
* Azure Foundry
* Azure Cloud Services
* SharePoint


