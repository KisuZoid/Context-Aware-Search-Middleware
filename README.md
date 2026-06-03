# Context-Aware Search Middleware

> Open-source middleware that injects context into search for better relevance.

Most search systems understand only the query.

Users search with much more than that:

* Current category
* Current page
* Session history
* Recent actions
* User preferences
* Business context

Context-Aware Search Middleware (CASM) sits between your application and search engine, transforming query-only search into context-aware search.

---

## Why

Traditional search:

```text
Search(query)
```

Context-aware search:

```text
Search(query, context)
```

Example:

Query:

```text
charger
```

Context:

```json
{
  "channel": "electronics"
}
```

Result:

```text
electronics charger
```

The same query can mean different things depending on where the user is and what they are doing.

---

## Architecture

```text
Application
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
```

---

## Supported Search Providers

Planned support for:

* Elasticsearch
* OpenSearch
* Algolia
* Typesense
* Vespa

---

## Example Request

```json
{
  "query": "charger",
  "context": {
    "channel": "electronics"
  }
}
```

Example response:

```json
{
  "original_query": "charger",
  "rewritten_query": "electronics charger"
}
```

---

## Roadmap

### v0.1 Foundation

* Context schema
* Query rewriting engine
* FastAPI service

### v0.2 Search Adapters

* Elasticsearch
* OpenSearch

### v0.3 Context Intelligence

* Context weighting
* Session awareness
* Re-ranking

### v1.0 Stable Release

* Production-ready API
* SDKs
* Search provider integrations

---

## Documentation

* Vision (`docs/vision.md`)
* Architecture (`docs/architecture.md`)
* Context Schema (`docs/context-schema.md`)
* Roadmap (`docs/roadmap.md`)

---

## Contributing

We welcome contributions, research, discussions, and adapter integrations.

See `CONTRIBUTING.md`.

---

## License

Apache License 2.0
