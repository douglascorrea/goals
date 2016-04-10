# Year long goals
- Create a cross platform application (Android and Web)
- Create an open source project
- Contribute to an open source project
- Continue and improve personal blog

# This week
- [x] Investigate how to use native components such as custom chrome tabs for react-native android (example of native UI components)
- [x] Add documentation to repo top level 
- [ ] Add documentation to repo for domain layer 
- [x] Add documentation to repo for web
- [ ] Add documentation to repo for react native 
- [x] See if nuclide will speed up react-native development
- [x] Investigate unit testing react components
- [ ] Investigate unit testing react native components
- [ ] Investigate unit testing redux reducers
- [x] Find ways to integration test domain-layer and web
- [ ] Find ways to integration test domain-layer and react-native
- [x] Investigate immutable.js
- [ ] Sweep floors in living, dining, and bed room
- [ ] Clean kitchen
- [ ] Clean bathroom
- [x] Buy filing cabinet from Walmart

# Week in review
I was able to setup unit testing for react components using the following packages: 
- enzyme for easy and intuitive api for interacting with the react components
- mocha for a test runner
- chai for an assertion library
- sinon for mocking 
- babel for compiling to es5 from es6

Overall I was very surprised on how easy it was to setup and how easy it is to test react components with enzyme. I was also able to leverage the full render and jsdom to have quick running integration tests for web. 

While I was exploring testing I also found out how to make [code snippets](https://github.com/atom/snippets) in Atom. They are much easier to create and use than IntelliJ's. 

Boilerplate reduction/test plan for redux 
- Action
  - DONE Use makeActionCreator from http://redux.js.org/docs/recipes/ReducingBoilerplate.html to create sync actions 
  - DONE only unit test this function 
  - unit test async action creator using https://github.com/arnaudbenard/redux-mock-store and https://github.com/node-nock/nock
- Reducers 
  - use https://github.com/indexiatech/redux-immutablejs for immutability and reducer creator 
  - use actions creators as part of reducer unit test to reduce boilerplate and since they are already tested
- Gaps 
  - true return values of async actions are not tested because they are mocked by nock, create a small number of happy path async integration between action creator and reducer 
- move actions consts reducers into single file since they go together
- look at async middleware to reduce boilerplate http://redux.js.org/docs/recipes/ReducingBoilerplate.html

Look into  [https://github.com/indexiatech/redux-immutablejs](https://github.com/indexiatech/redux-immutablejs) [http://appium.io/](http://appium.io/) for react native tests 

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
- `npm i --save-dev react-addons-test-utils mocha chai sinon enzyme jsdom babel-preset-es2015 babel-preset-react babel-register`
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
