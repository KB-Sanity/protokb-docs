---
sidebarDepth: 2
---

# Sidebar API

## registerTab
```ts
registerTab(plugin: ProtoPlugin, schema: SidebarSchema, options: SidebarTabOptions): TabAPI | void;
```
- **See also:**
    - [SidebarSchema](#sidebarschema)
    - [SidebarTabOptions](#sidebartaboptions)
    - [TabAPI](/api/tab.html)

## Types

### SidebarSchema
```ts
type SidebarSchema = (FormControl | FormBlock)[];
```
- **See also:**
    - [FormControl](#formcontrol)
    - [FormBlock](#formblock)

### FormControl
```ts
type FormControl =
    FormInputControl |
    FormSelectControl |
    FormColorControl;
```
- **See also:**
    - [FormInputControl](#forminputcontrol)
    - [FormSelectControl](#formselectcontrol)
    - [FormColorControl](#formcolorcontrol)

### FormInputControl
```ts
interface FormInputControl {
  control: FORM_CONTROL.INPUT; // 'input'
  label: string;
  key: string;
  type?: INPUT_CONTROL_TYPE; // 'number' | 'text'
  min?: number;
  max?: number;
  step?: number | string;
  default?: string | number;
  inline?: boolean;
  half?: boolean;
  description?: string;
}
```

### FormSelectControl
```ts
interface FormSelectControl {
  control: FORM_CONTROL.SELECT; // 'select'
  options: FormSelectControlOption[];
  label: string;
  key: string;
  description?: string;
  default?: string;
}
```
- **See also:** [FormSelectControlOption](#formselectcontroloption)

### FormSelectControlOption
```ts
interface FormSelectControlOption {
  title: string;
  value: string | number;
}
```

### FormColorControl
```ts
interface FormColorControl {
  control: FORM_CONTROL.COLOR; // 'color'
  label: string;
  key: string;
  default?: string;
  description?: string;
  inline?: boolean;
  half?: boolean;
}
```

### FormBlock
```ts
type FormBlock = FormHeaderBlock;
```
- **See also:** [FormHeaderBlock](#formheaderblock)

### FormHeaderBlock
```ts
interface FormHeaderBlock {
  block: FORM_BLOCK.HEADER; // 'header'
  size: `h${1 | 2 | 3 | 4 | 5 | 6}`;
  label: string;
  underline?: boolean;
}
```

### SidebarTabOptions
```ts
interface SidebarTabOptions {
  tabName: string;
  trigger: SIDEBAR_TAB_TRIGGER;
  onTrigger?: () => void;
  onCreate?: (tabApi: TabAPI) => void;
  onDestroy?: () => void;
}
```
- **See also:** [SIDEBAR_TAB_TRIGGER](#sidebar_tab_trigger)

### SIDEBAR_TAB_TRIGGER
```ts
enum SIDEBAR_TAB_TRIGGER {
  KEY_SELECTED,
}
```
