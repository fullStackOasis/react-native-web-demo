[This is where this repo came from.](https://github.com/fullStackOasis/react-native-web-demo) 👋 I'm Marya of fullStackOasis. Need mobile development work? Hit me up at fullstackdev@fullstackoasis.com.

This is a primer for using react-native-web to build a web client from your React Native project.

If you've got an existing React Native project, you **may** be able to compare this project with yours to figure out how (and if) you can turn your project into a web application.

In this case, we're starting with the default sample React Native project, and copying some demo code over from another demo.

The app runs on Android in development mode (with Metro server), as an apk, and also as a web application.

## The demo

A quick explanation of the demo: when running the usual `npx react-native@latest init AwesomeProject`, you'll get a very simple demo application.

The tutorials that I found for `react-native-web` used a demo that has a button you can tap to generate (and display) a new random number. I went with that to keep things as simple as possible during my journey into `react-native-web`. YMMV.

## Starting out

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

(In one terminal)

```
npx react-native start
```

(In second terminal)

```
npx react-native run-android
```

Worked for me.

## Build your apk

```
cd android
./gradlew clean
./gradlew assembleRelease
```