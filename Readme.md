# Year long goals
- Create a cross platform application (Android and Web)
- Create an open source project
- Contribute to an open source project
- Continue and improve personal blog

# This week
- [x] Investigate how to use native components such as custom chrome tabs for react-native android (example of native UI components)
- [ ] Add documentation to react native example repo
- [x] See if nuclide will speed up react-native development
- [x] Investigate unit testing react components
- [ ] Investigate unit testing redux reducers
- [ ] Find ways to integration test domain-layer and apps
- [ ] Investigate immutable.js
- [ ] Sweep floors in living, dining, and bed room
- [ ] Clean kitchen
- [ ] Clean bathroom
- [ ] Buy filing cabinet from Walmart

# Week in review
I was able to setup unit testing for react components using the following packages: 
- enzyme for easy and intuitive api for interacting with the react components
- mocha for a test runner
- chai for an assertion library
- sinon for mocking 
- babel for compiling to es5 from es6

Overall I was very surprised on how easy it was to setup and how easy it is to test react components with enzyme. I was also able to leverage the full render and jsdom to have quick running integration tests for web. 

While I was exploring testing I also found out how to make [code snippets](https://github.com/atom/snippets) in Atom. They are much easier to create and use than IntelliJ's. 

[https://github.com/indexiatech/redux-immutablejs](https://github.com/indexiatech/redux-immutablejs) [http://appium.io/](http://appium.io/) for react native tests

## Thoughts on nuclide
- mercurial support for things like blame and local change diff but not for git
- cannot get native inspector or debugger working
  - inspector does not see any devices
  - debugger will lock up device when running through nuclide

- makes atom startup slower
- I don't really understand flow but it adds some linting and go to definition.

Overall I do not think it is currently worth using.

## Thoughts on enzyme
Enzyme is a testing framework for React and React-Native
- simple and intuitive interface
- shallow render tests 
  - allow for true unit tests since errors in children are not propagated
  - can be used in web and native

- full render gives ability to interface with DOM when needed
  - could maybe used for integration tests?
  - only for web

- great documentation 
- ability to mix and match test runners, expectation libraries, and DOMS

## Setting up enzyme with mocha, chai, and sinon
- `npm i --save-dev react-addons-test-utils mocha chai sinon enzyme jsdom babel-preset-es2015 babel-preset-react babel-core`
- copy setup.js file [for jsom](http://airbnb.io/enzyme/docs/guides/jsdom.html)
- update .babelrc

```json
{
  "presets": ["es2015", "react"],
}
```

- add test script to package.json

```json
"scripts": {
    "test": "NODE_ENV=test node_modules/mocha/bin/mocha --compilers js:babel-register --require test/setup.js --recursive test/**/*Test.js"
  }
```

# Games of the week
