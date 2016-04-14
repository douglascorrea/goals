# Year long goals
- Create a cross platform application (Android and Web)
- Create an open source project
- Contribute to an open source project
- Continue and improve personal blog

# This week
- [x] Finish documentation to repo for domain layer 
- [x] Investigate unit testing react native components
- [x] Find ways to integration test domain-layer and react-native
- [x] Finish documentation to repo for react native 
- [ ] Find out how to authenticate to xbox live api with javascript

# Week in review
Enzyme is capable of unit testing react native components using its `shallow` rendering in combination with a JS mock of react native [`react-native-mock`](https://github.com/lelandrichardson/react-native-mock). Like with React, this testing approach is good for unit testing presentational components. 

For integration tests between multiple components or the domain layer an external tool such as [Appium](http://appium.io/) must be used. Tools like this have a higher learning curve than an API like Enzyme because they are external tools that black box test native apps. For this reason I don't really feel like messing with them right now. Most of these including Appium appear similar to cucumber and utilize some type of web driver to communicate with native devices. It may be worth looking into a framework that allows me to write the steps of the test once, and then rewrite the step definitions for the different UIs. 

# Games of the week
- Max Max
