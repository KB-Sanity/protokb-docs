---
sidebarDepth: 2
---

# Utils API

## pickFile
```ts
(accept?: string) => Promise<File>;
```

## saveFile
```ts
(content: string, fileName: string) => void;
```

## fileToText
```ts
(file: File) => Promise<string | ArrayBuffer>;
```