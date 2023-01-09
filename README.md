Resource to learn ReactJS in simple terms 

Go to https://sebastiandedeyne.com/react-for-vue-developers/

3 basic React Hooks are:
1. useState
2. useEffect
3. useContext

<ol>
<li>
<b>useState:</b> React uses a useState hook which returns a two-element array containing the current state value and a setter function.
<br><br>

```
import { useState } from 'react';

export default function ButtonCounter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      {count}
    </button>
  );
}
```

</li>

<li>
<b>useEffect:</b> It allows you to perform side effects in functional components, such as making an HTTP request or subscribing to a event listener.
To use useEffect, you simply need to call the hook inside your functional component and pass in a function that contains the side effects you want to perform. The hook will run this function after the component has finished rendering.
<br><br>

```
import { useState, useEffect } from 'react';

function DataFetcher() {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch('https://my-api.com/endpoint')
      .then(res => res.json())
      .then(data => setData(data));
  }, []);

  return (
    <div>
      {data ? <p>{data.name}</p> : <p>Loading...</p>}
    </div>
  );
}

```
</li>

<li>
<b>useContext:</b> The useContext hook is a way to access the context value inside a functional component. Context is a way to pass data through the component tree without having to pass props down manually at every level. To use useContext, you need to create a context using the React.createContext function, and then wrap the components that will be consuming the context with a Context.Provider component. You can then call the useContext hook inside a functional component to access the value of the context.
<br><br>

```
import { createContext, useContext } from 'react';

const ThemeContext = createContext('light');

function ThemeButton() {
  const theme = useContext(ThemeContext);
  return <button className={theme}>Click me</button>;
}

function App() {
  return (
    <ThemeContext.Provider value="dark">
      <ThemeButton />
    </ThemeContext.Provider>
  );
}

```

</li>
</ol>
