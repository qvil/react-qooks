# @react-qooks/use-axios

React Hook to fetch using axios.

## Install

```
npm i @react-qooks/use-axios
```

## Basic Usage

```js
import React from "react";
import useAxios from "@react-qooks/use-axios";

function App() {
  const render = useAxios(API_URL, fetchTrigger);

  return render({
    loading: () => <div>Loading</div>,
    error: error => <div>{error.toString()}</div>,
    data: data => <div>{JSON.stringify(data)}</div>
  });
}
```

## Advanced Usage

```js
import React, { useState } from "react";
import useAxios from "@react-qooks/use-axios";

function App() {
  const [fetchTrigger, setFetchTrigger] = useState(false);
  const render = useAxios(API_URL, fetchTrigger);

  return (
    <div>
      <button onClick={() => setFetchTrigger(true)}>Fetch</button>
      {render({
        loading: () => <div>Loading</div>,
        error: error => <div>{error.toString()}</div>,
        data: data => <div>{JSON.stringify(data)}</div>
      })}
    </div>
  );
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
| - data    | boolean  | Data from axios |
