# Header Slot

### Slot ID: `org.openedx.frontend.layout.header_profile.v1`

### Slot ID Aliases
* `header_slot`

## Description

This slot is used to replace/modify/hide the entire profile header.

## Example

The following `env.config.jsx` will replace the profile header entirely.

![Screenshot of custom component](./images/header_custom_component.png)

```js
import { DIRECT_PLUGIN, PLUGIN_OPERATIONS } from '@openedx/frontend-plugin-framework';

const config = {
  pluginSlots: {
    'org.openedx.frontend.layout.header_profile.v1': {
      keepDefault: false,
      plugins: [
        {
          op: PLUGIN_OPERATIONS.Insert,
          widget: {
            id: 'custom_header_component',
            type: DIRECT_PLUGIN,
            RenderWidget: () => (
              <h1>Header Slot</h1>
            ),
          },
        },
      ]
    }
  },
}

export default config;
```
