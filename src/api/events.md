---
sidebarDepth: 2
---

# Events API

## subscribe

- **Type**
```ts
subscribe<T extends keyof SystemEvent>(eventType: T, cb: SystemEvent[T]): void;
```
- **See also:** [SystemEvent](#systemevent)

## unsubscribe

- **Type**
```ts
unsubscribe<T extends keyof SystemEvent>(eventType: T, cb: SystemEvent[T]): void;
```
- **See also:** [SystemEvent](#systemevent)

## Types

### SystemEvent
```ts
interface SystemEvent {
  [EVENT.KEY_SELECTED]: (keyId: string) => void;
}
```
- **See also:** [EVENT](#event)

### EVENT
```ts
enum EVENT {
  KEY_SELECTED = 'key_selected',
}
```
