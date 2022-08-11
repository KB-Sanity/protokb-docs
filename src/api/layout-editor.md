---
sidebarDepth: 2
---

# Layout Editor API

## getKeyboard

- **Type**
```ts
getKeyboard(): KeyboardAPI;
```
- **See also:** [KeyboardAPI](/api/keyboard.html)

## getKeyboardData

- **Type**
```ts
getKeyboardData(): KeyboardData;
```
- **See also:** [KeyboardData](#keyboarddata)

## setKeyboardData

- **Type**
```ts
setKeyboardData(data: KeyboardData): Promise<void>;
```
- **See also:** [KeyboardData](#keyboarddata)

## Types

### KeyboardData
```ts
interface KeyboardData {
  version: string;
  keyCaps: KeyCapData[];
  plugins: PluginsData;
}
```
- **See also:** [PluginsData](#pluginsdata)

### PluginsData
```ts
type PluginsData = PluginData[];
```
- **See also:** [PluginData](#plugindata)

### PluginData
```ts
interface PluginData {
  id: string;
  data: any;
}
```
