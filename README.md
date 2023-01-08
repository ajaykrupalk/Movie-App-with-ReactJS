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
</ol>
