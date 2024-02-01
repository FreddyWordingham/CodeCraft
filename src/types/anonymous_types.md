# Anonymous Types

Types defined inline without a name, typically for short-lived, simple data structures. Useful for quick and local data grouping without the need to define a formal class or struct.

```typescript
// Define an anonymous type (object literal)
const person = {
  name: "Alice",
  age: 30,
};

// Access properties of the anonymous type
console.log(`Name: ${person.name}, Age: ${person.age}`);
```
