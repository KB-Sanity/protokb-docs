---
sidebarDepth: 2
---

# Toolbar API

## registerButtons

- **Type**
```ts
registerButtons(plugin: ProtoPlugin, btns: ToolbarButtonOptions[]): void;
```

## Types

### ToolbarButtonOptions

```ts
interface ToolbarButtonOptions {
  name: string;
  icon: ToolbarButtonIcon;
  size?: number;
  onClick?: () => any;
}
```
`ToolbarButtonIcon` - PascalCase icon name from [Feather](https://feathericons.com/) library