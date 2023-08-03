# Sample React-Native-Web App
## _Code architecture followed by 55Tech developers._

✨ This repository showing that how we are using clean code architecture, folder structure, and component reusability.✨

## Features

- _**Functionality**_  : Work correctly, efficiently, and robustly.
- _**Readability**_    : The primary audience for our code is other developers.
-  _**Extensibility**_ : Well-designed code should be extensible as a building block for solving new problems.
- _**Scalability**_    : The code that can scale along with the need of your business.
- _**Testability**_    : Isolated and modularised code without dependencies, well testable at unit level.

## Tech

- [React Native](https://reactnative.dev/) - An open-source UI software framework created by Meta Platforms, Inc for building beautiful, natively compiled, multi-platform applications from a single codebase.
- [React native web](https://github.com/necolas/react-native-web) - Run React Native components and APIs on the web using React DOM
- [Web pack](https://webpack.js.org/) - Bundle your JavaScript applications.
- [Redux Toolkit](https://redux-toolkit.js.org/) - Easier to write good Redux applications and speeds up development
- [StoryBook](https://storybook.js.org/) - Organizes every UI component and its stories and run it in a separate node process from the app.
- [React Native Paper](https://reactnativepaper.com/) - Cross-platform UI kit library containing a collection of customizable and production-ready components and to support custom themes
- [Reacti18next](https://react.i18next.com/getting-started) - Helps to translate your JSON internationalization files
- [React navigation](https://reactnavigation.org/docs/getting-started/) - Enables to implement navigation functionality
- [React Native Firebase](https://rnfirebase.io/) - Officially recommended collection of packages that brings React Native support for all Firebase services on both Android and iOS apps.
- [Axios](https://axios-http.com/) - Promise based HTTP client which provides a simple to use library in a small package with a very extensible interface.
- [Netinfo](https://github.com/react-native-netinfo/react-native-netinfo) - Helps to get Network Info for Android, iOS and macOS

## Config variables
- [react-native-config](https://github.com/luggit/react-native-config) - Module to expose config variables in Android and Ios
- [dotenv-webpack](https://www.npmjs.com/package/dotenv-webpack) - for web

## Basic requirements

* Git  [Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* XCode [Install XCode](https://developer.apple.com/xcode/)
* Android studio [Install Android studio](https://developer.android.com/studio)

## Installation/Setup guide

### 1. Install dependencies
```sh
# Clone the example app repo
git clone https://github.com/FiftyfiveTech/sample-reactnative-webapp
```
```sh
#open terminal and navigate to the cloned directory
cd sample-reactnative-webapp
```
```sh
# Install dependencies
yarn
```
### 2. run your app 
```sh
# run on web 
yarn run web 
open http://localhost:8080/ in your browser
```
```sh
# run on android 
yarn run android 
```
```sh
# run on ios
cd ios && pod install 
cd ..
yarn run ios
```
```sh
# Start storybook on web 
yarn storybook
```
```sh
# Build storybook for web
yarn build-storybook
```

## Archirecture and Project structure

This project follows the `Clean Architecture`, and hence have focused the structuring of the project on the standard practices that are recommended by the `Clean Architecture`. You will find we have focused on `de-coupling` and `reusability` of the code

```

├── .git
├── .gitignore
├── .storybook
├── android
├── assets
|  └── fonts
|  └── image
├── Components
|  └── Button
|  └── TextView
|  └── RadioButton
├── ios
├── patches
├── src
|  ├── containers
|  |  └── button
|  |  └── icon
|  |  └── text
|  |  └── textinput
|  ├── core
|  |  └── interfaces
|  |  └── reducers
|  |  └── store
|  |  └── thunk
|  ├── i18n
|  ├── locales
|  ├── navigation
|  ├── screens
|  |  ├── Home
|  |  ├── Login
|  |  ├── Signup
|  ├── theme
|  ├── util
├── web
|  └── index.html
├── App.tsx
├── README.md
├── app.json
├── index.tsx
├── index.web.tsx
├── metro.config.json
├── package.json
├── react-native.config.json
├── tsconfig.json
├── tslint.json
```

**assets** - It will have all the font files and the icons that are gonna be used throughout the project.

**components** - It will have all the components like button, text, textInput, Image, listview, radioButtons etc. which will accept props from parent view and return the component accordingly.

**container** - It will have the wrappers like base View of every screen or button View etc. created which are going to be consistent throughout the app and which will be according to the design patterns being followed and used for the app.

**core** - It will have the store, reducers and thunk related files.

**locales** - It will have the strings/copy defined being used throughout the app. This will also support the multi language translations.

**navigation** - It will have all the navigation stack(s) and screen navigations.

**screen** - It will have all the main/parent screens that are gonna be there in the app. Any child/sub view/screen should be defined in the main screen folder.

**theme** - It will have all the colors and common styles defined which will be according to the color,font and design schema given by the designers.

**util** - It will have all the miscellaneous code like common functions, constants, some helper methods etc.


## Expected coding standards in the code:

1. The code should be linted using Eslint before committing the code.
2. There should not be any hard coded string in the code. All of the Strings should be defined in [locales](./src/locales).
3. The `Early Return` pattern should be used in the code for the `if` statements. More on this could be found in the links:
    - [Return early pattern](https://github.com/founderandlightning/coding-guidelines/blob/master/JavaScript/README.md#follow-return-early-pattern)
    - [Clean else statements](https://www.geeksforgeeks.org/writing-clean-else-statements/)
    - [Avoid else](https://blog.timoxley.com/post/47041269194/avoid-else-return-early)
    - [Prevent using if else statements](https://medium.com/@janalmazora/how-to-prevent-using-if-else-statements-in-your-code-7e05e43afde)
4. Proper API error handling should be there.
5. Destructuring should be there for the objects like `state` and `props`.
7. We should try to make our commits smaller but more often.
8. Remove unused code and logs before committing the code.

## License

**55 Tech**

**We are relentlessly focusing on digital transformation. Dive deep into the customer cases to know more about the project which we delivered.**