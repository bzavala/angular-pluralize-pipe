# angular-pluralize-pipe
A pipe for pluralizing a word based on a 'count' parameter
---
Example usage in Angular template

```
@for(word of words; track word) {
  {{ word | pluralize : words.length }}
}
```
