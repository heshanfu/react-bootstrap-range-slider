# React Bootstrap Range Slider

A range slider component for React Bootstrap (Bootstrap 4) that extends the native HTML `<input type="range">` element.

<img src="./screenshots/react-bootstrap-range-slider-screenshot.png?raw=true" alt="React Bootstrap Range Slider screenshot showing rendered slider component with various options applied, including label placement and different variants" width="479">

## Installation

    npm install react-bootstrap-range-slider

### Prerequisites

React Bootstrap and Bootstrap must be installed and the CSS from Bootstrap imported.

## Usage

```JavaScript
import React, { useState } from 'react';
import 'react-bootstrap-range-slider/dist/react-bootstrap-range-slider.css';
import RangeSlider from 'react-bootstrap-range-slider';

const MyComponent = () => {

  const [ value, setValue ] = useState(0); 

  return (
    <RangeSlider
      value={value}
      onChange={changeEvent => setValue(changeEvent.target.value)}
    />
  );

};
```

## Options (as React props)

| Property | Type | Default | Description |
| --- | --- | --- | --- |
| `value` | `number` | | **Required.** The current value of the slider. |
| `onChange` | `function` | |  **Required.** A callback fired when the value prop changes. |
| `min` | `number` | `0` | The minimum value of the slider. |
| `max` | `number` | `100` | The maximum value of the slider. |
| `step` | `number` | `1` | The granularity with which the slider can step through values. |
| `disabled` | `boolean` | `false` | Disables the slider. |
| `size` | `'sm'` \| `'lg'` | | Input size variants, for compatibility with other Bootstrap form components. |
| `variant` | `string` | `'primary'` | Color variant, equivalent to the Bootstrap Button color variant. One of: `'primary'`, `'secondary'`, `'success'`, `'danger'`, `'warning'`, `'info'`, `'dark'`, `'light'` |
| `tooltip` | `'auto'` \| `'on'` \| `'off'` | `'auto'` | If `'auto'` the tooltip will be visible only when hovered. If `'on'` the tooltip will always be visible. If `'off'` no tooltip will be displayed.  |
| `tooltipPlacement` | `'top'` \| `'bottom'` | `'bottom'` | Placement of tooltip relative to slider thumb. |
| `tooltipLabel` | `function` | | A function that returns the tooltip's content (either a string or element). The function's first argument is the current slider value. |
| `inputProps` | `object` | | Properties applied to the `<input>` element. |
| `ref` | `ReactRef` | | If provided, ref will be forwarded to the underlying `<input>` element. |
| `bsPrefix` | `string` | `'range-slider'` | Change the underlying component CSS base class name and modifier class names prefix. **This is an escape hatch** for working with heavily customized bootstrap css. |

## License

Copyright (c) 2020 Jason Wilson

[MIT License](LICENSE)
