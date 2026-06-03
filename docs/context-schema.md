# Context Schema v1

## Request

```json
{
  "query": "charger",
  "context": {
    "channel": "electronics",
    "page": "mobile-accessories",
    "session": [],
    "user": {},
    "location": "india"
  }
}
```

---

## Context Fields

### channel

Current business category.

Examples:

* electronics
* beauty
* grocery
* books

---

### page

Current page or section.

Examples:

* mobile-accessories
* laptop-category
* skincare

---

### session

Sequence of recent user actions.

Examples:

```json
[
  "laptop",
  "mouse",
  "charger"
]
```

---

### user

Optional user metadata.

Examples:

```json
{
  "segment": "student",
  "language": "en"
}
```

---

### location

User region.

Examples:

```text
india
usa
germany
```

---

## Design Principles

* Explicit
* Portable
* Search-provider agnostic
* Backward compatible
