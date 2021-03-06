---
nav:
  path: /utilities
---

# getPluginData

Retrieves custom information that was stored on the node or style using `setPluginData`. Wraps around native `setPluginData` with safe check.

## Example

```tsx
import { getPluginData, setPluginData } from 'figx';
const frame = figma.createFrame();
setPluginData('count', '1');
getPluginData(frame, 'count'); // '1'
```

## API

```ts
const value = getPluginData(node, key);
```

### Params

| Property | Description                       | Type                | Default |
| -------- | --------------------------------- | ------------------- | ------- |
| node     | The node to hold the storage data | `Partial<BaseNode>` | -       |
| key      | Storage key                       | `string`            | -       |

### Result

| Property | Description  | Type     |
| -------- | ------------ | -------- |
| value    | Storage data | `string` |
