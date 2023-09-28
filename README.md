This project is based on a new [**React Native**](https://reactnative.dev) project, bootstrapped using [`@react-native-community/cli`](https://github.com/react-native-community/cli).

This is just the default React Native app.

Make sure you can build a regular React Native app (the simplest possible example is fine) before proceeding.

Next, follow the instructions by [Kumar Harsh](https://blog.logrocket.com/complete-guide-react-native-web/) under the section "Adding React Native web support using CRA".

```
mkdir public
touch public/index.html
```

After doing this, make sure that your index.html file looks like the one in this project or at [create-react-app](https://github.com/facebook/create-react-app/blob/main/packages/cra-template/template/public/index.html) which is where I got mine.

```
npm install react-native-web react-scripts react-dom
```

In root of project, do:

```
mv index.js index.native.js
mkdir src
touch src/index.js
```

Make sure your `src/index.js` looks like the one in this project, which points to `src/App.js`. Notice that we're skipping over the default `App.tsx`.

Edit `index.native.js` to look like the one in this project.

Add scripts (if desired) to `package.json`.

## Running on Web

Running `npm run web` just worked for me at this point. View the app in your browser at localhost:3000.

## Running on Android

Just do:

```
npx react-native run-android
```

Worked for me.