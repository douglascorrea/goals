# Year long goals
- Create a cross platform application (Android and Web)
- Create an open source project
- Contribute to an open source project
- Continue and improve personal blog

# This week
- [x] Get react-redux counter sample working on both web and android
- [ ] Get react-redux sample with network calls working on both web and android
- [ ] Investigate how to use native components such as custom chrome tabs for react-native android (example of native UI components)
- [x] Investigate if native Java code can be used in react-native android (example of native modules)
- [ ] Finish going browsing react-native docs
- [ ] Push examples to a repository and add some documentation for it

# Week in review
Next week I would like to investigate testing focusing on unit testing react components and redux reducers as well as integrations tests. I would also like to look into using the gradle daemon.

# Learned this week
Thoughts on React-native, React and Redux

Pros
- React and react-native have hot swapping when setup properly!! This is amazing on android.
- Can share domain layer (actions, reducers, store) between different UIs such as web, android, and ios.
- Large community and number of useful packages compared to others such as Elm

Cons
- `react-native run-android` fails half the time because of `com.android.builder.testing.api.DeviceException: com.android.ddmlib.InstallException: Unable to upload some APKs`
  - This can be solved by changing gradle version to 1.2.3 in build.gradle file
- Cryptic and very unhelpful error message from react and react-native, makes me miss Elm :'(
- Ecosystem is overwhelming to get started with (ES6, Babel, Webpack, Node, Npm, etc.)
- Still Javascript (no type safety, pointless testing to ensure everything hooked up properly, etc.)

# Games of the week
- Max Max
