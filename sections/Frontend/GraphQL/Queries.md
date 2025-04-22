# 📡 GraphQL Queries

This document lists the key GraphQL queries used in the [PORTAL_NAME] portal.

## Query: [QUERY_NAME]

```graphql
query ExampleQuery($param1: String!, $param2: Int) {
  entity(id: $param1) {
    id
    name
    details {
      field1
      field2(filter: $param2)
    }
    relatedItems {
      id
      title
    }
  }
}
```

### Usage
- **Purpose**: [What this query is used for]
- **Components**: [List of components using this query]
- **Variables**:
  - `param1`: [Description and purpose]
  - `param2`: [Description and purpose]
- **Microservice**: [Which microservice handles this data]

### Response Structure
```typescript
interface QueryResponse {
  entity: {
    id: string;
    name: string;
    details: {
      field1: string;
      field2: number[];
    };
    relatedItems: {
      id: string;
      title: string;
    }[];
  };
}
```

### Performance Considerations
- **Caching Strategy**: [Cache-control details]
- **Fetch Policy**: [Apollo fetch policy used]
- **Typical Response Size**: [Approximate size]

---

## Query: [QUERY_NAME_2]

```graphql
query AnotherExampleQuery($filter: FilterInput!) {
  searchEntities(filter: $filter) {
    totalCount
    items {
      id
      title
      status
    }
  }
}
```

### Usage
- **Purpose**: [What this query is used for]
- **Components**: [List of components using this query]
- **Variables**:
  - `filter`: [Description and purpose]
- **Microservice**: [Which microservice handles this data]

### Response Structure
```typescript
interface SearchResponse {
  searchEntities: {
    totalCount: number;
    items: {
      id: string;
      title: string;
      status: string;
    }[];
  };
}
```

### Performance Considerations
- **Caching Strategy**: [Cache-control details]
- **Fetch Policy**: [Apollo fetch policy used]
- **Typical Response Size**: [Approximate size]