# Music Player Application

## Expo Setup

```bash
yarn create expo-app . -t

npx expo lint

yarn add -D prettier eslint-config-prettier eslint-plugin-prettier eslint-plugin-react-native

yarn lint --fix
```

```js
module.exports = {
  extends: ["expo", "prettier"],
  plugins: ["prettier", "react-native"],
  rules: {
    "prettier/prettier": "error",
    "react-native/no-unused-styles": "error",
  },
};
```

## Expo Router Setup

```bash
npx expo install expo-router react-native-safe-area-context react-native-screens expo-linking expo-constants expo-status-bar

"main": "expo-router/entry"

"scheme": "plantly"
```

create app folder and move App.tsx to that and change to index.tsx and create _layout.tsx

## NativeWind Setup

```bash
npx expo install nativewind tailwindcss react-native-reanimated react-native-safe-area-context

npx tailwindcss init
```

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  // NOTE: Update this to include the paths to all of your component files.
  content: ["./app/**/*.{js,jsx,ts,tsx}"],
  presets: [require("nativewind/preset")],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

[expo-router nativewind](https://www.nativewind.dev/getting-started/expo-router)

[typescript nativewind](https://www.nativewind.dev/getting-started/typescript)

## Development Build

```bash
npx expo install expo-dev-client

npx expo prebuild --platform ios
npx expo prebuild --platform android

npx expo run:ios
npx expo run:android
```
