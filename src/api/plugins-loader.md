---
sidebarDepth: 2
---

# Plugins Loader API

## getPlugins
- **Type**
```ts
getPlugins(): string[];
```

## getExternalPlugins
- **Type**
```ts
getExternalPlugins(): string[];
```

## getPluginApi
- **Type**
```ts
getPluginApi(id: string): any;
```

## getPluginInfo
- **Type**
```ts
getPluginInfo(id: string): Omit<Plugin, 'instance'>;
```
- **See also:** [Plugin](#plugin)

## getPluginData
- **Type**
```ts
getPluginData(id: string): any;
```

## Types

### Plugin
```ts
interface Plugin<T extends ProtoPlugin = ProtoPlugin> {
  name: string;
  description: string;
  id: string;
  url?: string;
  instance: T;
}
```