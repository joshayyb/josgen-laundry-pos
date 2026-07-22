# Coding Standards

## Stack
- Kotlin
- Jetpack Compose
- MVVM
- StateFlow
- Repository pattern

## Flow
```text
Composable
→ ViewModel
→ Use Case
→ Repository
→ Firestore / Printer / Local Cache
```

## Rules
- No Firestore calls in Composables
- No business logic in Composables
- Immutable UI state
- Validation in domain/use-case layer
- Append-only payments and adjustments
- Use server timestamps
- Avoid floating-point arithmetic for money
- Use clear domain names
- Never swallow exceptions silently
