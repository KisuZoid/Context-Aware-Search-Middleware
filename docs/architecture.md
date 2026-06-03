# Architecture

## High-Level Flow

```text
Application
     ↓
Context Collector
     ↓
Context Engine
     ↓
Query Rewriter
     ↓
Search Adapter
     ↓
Search Provider
     ↓
Result Re-ranker
     ↓
Application
```

---

## Components

### Context Collector

Collects contextual signals from the host application.

Examples:

* Current category
* Current page
* Session history
* User segment

---

### Context Engine

Processes and weights contextual signals.

Responsibilities:

* Signal prioritization
* Context scoring
* Context validation

---

### Query Rewriter

Transforms queries based on context.

Example:

```text
charger
```

↓

```text
electronics charger
```

---

### Search Adapter

Provides compatibility with:

* Elasticsearch
* OpenSearch
* Algolia
* Typesense

---

### Result Re-ranker

Adjusts ranking using contextual relevance scores.
