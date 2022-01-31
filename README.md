# use-sticky-state

Custom hook to persist React state on browser

If you're looking to persist React Native state, check out [react-native-sticky-state](https://www.npmjs.com/package/react-native-sticky-state)

## ⚙️ Installation

In your React project folder, run:

```bash
npm i use-sticky-state --save
```

## 💻 Example

```js
import useStickyState from "use-sticky-state";

const App = () => {
  const [count, setCount] = useStickyState(0, "counter-key");

  return (
    <div>
      <button onClick={() => setCount(count + 1)}>Increment</button>

      <p>{count}</p>
    </div>
  );
};
```

## 📚 Usage

```js
const [state, setState] = useStickyState(defaultValue, storageKey);
```

| Property     | Description                                                                                                                                                    |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| defaultValue | The default value used if storageKey was not previously set                                                                                                    |
| storageKey   | Unique string key used to persist data, using your browser's built in [localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) API |
