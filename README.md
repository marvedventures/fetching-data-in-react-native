# HTTP Request/Response in React Native

Fetching REST API in React Native

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### Screenshot

![image](https://user-images.githubusercontent.com/108392678/213912434-c6db769b-7d43-4bcb-9ea3-1494b65e6e9e.png)
![image](https://user-images.githubusercontent.com/108392678/213912419-8471e5c7-1568-465b-8c16-2a768f29d021.png)


### Links

- Github: [Code](https://github.com/marvedventures/fetching-data-in-react-native)

## My process

### Built with

- [React Native](https://reactnative.dev/docs/environment-setup) - React Native using Expo Go
- [FlatList](https://reactnative.dev/docs/flatlist) - For lazy rendering menu items
- [StyleSheet](https://reactnative.dev/docs/stylesheet) - For styles

### What I learned

- Create a React Native App using Expo
- Fetching data using Fetch API
- Using async/ await
- Storing fetched data in a state
- Handling side-effects using useEffect Hook
- Use SafeAreaView, View, Text, and FlatList Components
- Create a component to display menu items and use FlatList
- Extract all styles to StyleSheet API

Here is a code snippet:

```jsx
const [data, setData] = useState([]);

const getMenu = async () => {
  try {
    const response = await fetch("https://...");
    const json = await response.json();
    setData(json.menu);
  } catch (error) {
    console.error(error);
  } finally {
    setLoading(false);
  }
};

useEffect(() => {
  getMenu();
}, []);
```

### Useful resources

- [React Native Docs (StyleSheet) ](https://reactnative.dev/docs/stylesheet) - This helped me for all the neccessary React Native styles. I really liked their documentation and will use it going forward.
- [React Native Docs (FlatList) ](https://reactnative.dev/docs/flatlist) - This helped me for lazy loading the Menu Lists.
- [React Docs (useEffect) ](https://reactjs.org/docs/hooks-reference.html#useeffect) - This helped me for handling side-effects and fetching data in React.

## Author

- Website - [Marvin Morales Pacis](https://marvin-morales-pacis.vercel.app/)
- LinkedIn - [@marvedventures](https://www.linkedin.com/in/marvedventures/)
- Twitter - [@marvedventures](https://www.twitter.com/marvedventures)
