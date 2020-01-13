# react-native-fade-in-view [![npm version](https://badge.fury.io/js/react-native-fade-in-view.svg)](https://badge.fury.io/js/react-native-fade-in-view)
> A simple and lightweight RN component that fades in its children

## Install
`yarn add react-native-fade-in-view` or `npm install react-native-fade-in-view --save`

## API
### `onFadeComplete`
A function that is called when the fade animation completes

### `duration`
The duration of the fade animation, **`500ms`** by default

### `delay`
The time to wait (in milliseconds) before the fade starts, **`0ms`** by default

### `style`
Style to be given to the view

## Usage

### Basic Usage
```javascript
import FadeInView from 'react-native-fade-in-view';

const myFadeInComponent = () => (
  <FadeInView
    duration={750}
    style={{ alignItems: 'center' }}
    onFadeComplete={() => alert('Ready')}
  >
    <Text>This view will fade in nicely</Text>
  </FadeInView>
);
```

### Cascading List View
```javascript
import FadeInView from 'react-native-fade-in-view';

// Assuming items is an array of components
const myFadeInList = () => (
  <ScrollView> 
    {items.map((item, i) => (
      <FadeInView key={i} delay={i * 20}>
        {item}
      </FadeInView>
    ))}
  </ScrollView>
);
```
