# IntentGraph

[中文说明](./README.zh-CN.md)

IntentGraph is a minimal Blueprint/Graph framework for gameplay logic.

The project is intentionally starting small. The near-term goal is not to build a giant visual scripting platform, but to establish an extensible core loop that can grow through real game development and UGC needs.

## AI-Friendly Graph

IntentGraph is not trying to become a traditional Blueprint system.

It is better understood as an AI-friendly graph for gameplay logic: a structured, text-first, schema-driven representation that AI can read, generate, patch, validate, and extend with much higher reliability than a purely editor-centric workflow.

At the current stage of AI tooling, this direction is meant to make game production faster and more practical. The goal is to help teams build gameplay logic more efficiently with AI, instead of recreating the full shape of older visual scripting tools.

## Vision

IntentGraph focuses on a practical, text-first representation of gameplay logic:

- describe graphs in text
- define node schemas
- register nodes into a runtime registry
- validate graph structure and data
- execute a minimal runtime graph
- update graphs through patches

The first target scenario is trigger-driven gameplay logic, such as devices, mechanisms, and interactive level events.

## Current Goal

The current milestone is to build a minimal `blueprint-core` with:

- textual graph description
- node schema definition and registration
- basic validation
- a minimal executor
- examples and patch support
- a workflow that is friendly to AI-assisted node authoring and expansion

## Product Direction

IntentGraph will add nodes gradually through real UGC requirements instead of trying to design a complete node ecosystem up front.

That means:

- the core should stay small and extensible
- new nodes should be added because a real gameplay case needs them
- data format, validation, and execution should remain stable as the node set grows

## What This Project Is Not

IntentGraph is intentionally not trying to do the following right now:

- a traditional Blueprint clone
- a GUI editor
- a full UGC platform
- a general-purpose scripting language
- a huge all-in-one node library
- a complex subgraph or inheritance system
- Unreal Engine Blueprint feature parity

## Why This Shape

Many gameplay logic systems fail by becoming too broad too early. This project takes the opposite approach:

- start from a minimal closed loop
- prove it in one concrete gameplay category
- expand only after real usage exposes the next missing piece

It also reflects a different assumption: in this phase of AI development, the most useful gameplay graph is not necessarily the most visual one. It is the one that is easiest for humans and AI to co-author, inspect, patch, validate, and execute.

The expectation is that a small, reliable core will be more useful than a large but vague framework.

## Phase 1 Focus

Phase 1 is centered on trigger and mechanism logic, for example:

- trigger -> condition -> action
- device activation chains
- interactive level events
- simple event-driven gameplay flows

This scope is small on purpose. It is enough to validate the schema/graph/registry/validator/executor/patch pipeline before moving into more advanced systems.

## Status

The repository is currently focused on defining the foundation and direction of the framework. The main objective is to make the core loop extensible first, then grow the node set and surrounding tooling incrementally.
