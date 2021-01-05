# React TSX Style Guide

## Table of Contents

  1. [Scope](#scope)
  1. [Basic Rules](#basic-rules)
  1. [Naming](#naming)

## Scope

- React with Hooks support
- Typescript

## Basic Rules

- TS: Avoid `any` typing

## Naming

- **Component**: use `PascalCase`

Directory: `[ComponentName]`

Entry point: `index.tsx`

Module CSS: `[ComponentName].module.css`

Subcomponent: Similar as component but inside component's directory

**Example**: `[ComponentName]/index.tsx`, `[ComponentName]/[ComponentName].module.css`, `[ComponentName]/[SubComponentName]/index.tsx`

 - **Props**: use `camelCase`

```jsx
<MyComponent name="My Modal" isOpen={true}  />
```

- **Variables**: use `camelCase`

- **Constants**: use `NAMES_LIKE_THIS` style

```jsx
const MAX_ITEM_NUMBER = 3
```

- **Hooks**: Prefix `use` with hook name `use[YourCustomHook].ts`

**Example**: `useInitNotification.ts`

- **Others**: Use `camelCase` for file and directory

**Example**: `profileService.ts`

## Component

Use **Function Component** is recommended

```jsx

function Example() {
  return <div>Hello World</div>
}

```

- **Props**: 

Try to limit number of props as few as possible, use **optional** props if possible

```jsx

type TProps = {
  name: string, // required prop
  description?: string // optional prop
}

function Example({name, description = ''}: TProps) {
  return <div>Hello {name}, {description}</div>
}

// Using the component

<Example name="Nhan" />

```


**[⬆ back to top](#table-of-contents)**
