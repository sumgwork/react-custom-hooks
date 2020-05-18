# react-custom-hooks

> Useful list of custom React hooks

[![NPM](https://img.shields.io/npm/v/@sgovil/react-custom-hooks)](https://www.npmjs.com/package/@sgovil/react-custom-hooks)
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
[![demo site](https://img.shields.io/badge/demo-site-green)](https://sumgwork.github.io/react-custom-hooks/)

## Install

```bash
npm install --save @sgovil/react-custom-hooks
```

## Usage

```jsx
import React from "react";
import useFetch from "@sgovil/react-custom-hooks";

export default function App() {
  const [response, error, loading] = useFetch(
    "https://jsonplaceholder.typicode.com/todos"
  );
  return (
    <div>
      <h1>React Custom Hooks</h1>

      {loading && <div>Loading...</div>}
      {!loading && error && <div>{error.message}</div>}
      {!loading && !error && response && (
        <div>
          <h2>Fetch Complete</h2>
          <pre>{JSON.stringify(response, undefined, 2)}</pre>
        </div>
      )}
    </div>
  );
}
```

## License

MIT © [sumgwork](https://github.com/sumgwork)

---

This hook is created using [create-react-hook](https://github.com/hermanya/create-react-hook).
