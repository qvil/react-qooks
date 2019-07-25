# @react-qooks/use-debounce

React Hook to debounce.

## Install

```
npm i @react-qooks/use-debounce
```

<!-- ## Basic Usage

[Live Demo(Code Sandbox)](https://codesandbox.io/embed/react-qooksuse-axios-basic-example-uige8)

```js
import React from "react";
import useAxios from "@react-qooks/use-axios";

function App() {
  const render = useAxios(API_URL);

  return render({
    loading: () => <div>Loading</div>,
    error: error => <div>{error.toString()}</div>,
    data: data => <div>{JSON.stringify(data)}</div>
  });
}
```

## Parameters

| Parameter | Type    | Description                                                              | Required | Default Value |
| --------- | ------- | ------------------------------------------------------------------------ | -------- | ------------- |
| url       | string  | API URL                                                                  | yes      | undefined     |
| autoFetch | boolean | Fetch trigger, If you want to not fetch automatically set value to false | no       | true          |

## Return value

| value     | Type     | Description     |
| --------- | -------- | --------------- |
| callback  | function | render function |
| - loading | boolean  | Loading state   |
| - error   | boolean  | Error           |
| - data    | boolean  | Data from axios | -->
