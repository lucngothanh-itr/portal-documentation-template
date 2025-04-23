# 📡 GraphQL Mutations

This document lists the key GraphQL mutations used in the [PORTAL_NAME] portal.

## Mutation: [MUTATION_NAME]

```graphql
mutation UpdateEntity($id: ID!, $input: EntityUpdateInput!) {
  updateEntity(id: $id, input: $input) {
    id
    name
    status
    updatedAt
  }
}
```

### Usage

- **Purpose**: [What this mutation is used for]
- **Components**: [List of components using this mutation]
- **Variables**:
  - `id`: [Description and purpose]
  - `input`: [Description and purpose]
- **Microservice**: [Which microservice handles this operation]

### Input Structure

```typescript
interface EntityUpdateInput {
  name?: string;
  status?: string;
  attributes?: {
    key: string;
    value: string;
  }[];
}
```

### Response Structure

```typescript
interface UpdateEntityResponse {
  updateEntity: {
    id: string;
    name: string;
    status: string;
    updatedAt: string;
  };
}
```

### Error Handling

- **Validation Errors**: [How validation errors are handled]
- **Authorization Errors**: [How authorization errors are handled]
- **Optimistic Updates**: [Whether optimistic updates are used]

---

## Mutation: [MUTATION_NAME_2]

```graphql
mutation CreateEntity($input: EntityCreateInput!) {
  createEntity(input: $input) {
    id
    name
    status
    createdAt
  }
}
```

### Usage

- **Purpose**: [What this mutation is used for]
- **Components**: [List of components using this mutation]
- **Variables**:
  - `input`: [Description and purpose]
- **Microservice**: [Which microservice handles this operation]

### Input Structure

```typescript
interface EntityCreateInput {
  name: string;
  status: string;
  type: string;
  attributes?: {
    key: string;
    value: string;
  }[];
}
```

### Response Structure

```typescript
interface CreateEntityResponse {
  createEntity: {
    id: string;
    name: string;
    status: string;
    createdAt: string;
  };
}
```

### Error Handling

- **Validation Errors**: [How validation errors are handled]
- **Authorization Errors**: [How authorization errors are handled]
- **Optimistic Updates**: [Whether optimistic updates are used]
