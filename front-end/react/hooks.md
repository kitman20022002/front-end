# Hooks 

### Key Points
- Hooks allow function components to have access to state 
- Only for function compoment



## React Defined Hooks 
### useState() : 
- Allows us to track state in a function component
- Returns a stateful value, and a function to update it
- State generally refers to data or properites that need to be tracking in an application

#### How does it work ? 
- Returns a stateful value, and a function to update it

tells react that your compoment needs to do something after render. Similar to CompomentDidMound and componentWillUnmount
```
import React, { useState, useEffect } from 'react';

function FriendStatus(props) {
  const [isOnline, setIsOnline] = useState(null);

  if (isOnline === null) {
    return 'Loading...';
  }
  return isOnline ? 'Online' : 'Offline';
}
  ```
  You might be thinking that we’d need a separate effect to perform the cleanup. But code for adding and removing a subscription is so tightly related that useEffect is designed to keep it together. If your effect returns a function, React will run it when it is time to clean up:

### useEffect(): 
- Allows you to perform side effects in your components: side effects = fetching data, directly updating the DOM, and timers.
- By default, effects run after every completed render
- But you can choose to fire them only when certain values have changed

### useContext():
- A way to manage state globally
- It can be used together with the useState Hook to share state between deeply nested components more easily than with useState alone.
