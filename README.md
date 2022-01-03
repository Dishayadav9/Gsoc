# Eos-icons
Enhancing Backend and introduction of new features for EOS icons
# Eos-icon picker
[![Open Source Love svg2](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)

### | Main changes:
The code got refactored/re-written in typescript.
The system is now depending on the Mongo database as main source of truth.
Caching layer is introduced to make the process of fetching the icons faster.
Algolia services is introduced to be used for the search queries.
A validation layer using Joi is added to validate all the incoming requests.
A unit tests using Mocha and Chai are written to ensure that all the new APIs are working as expected.
A Docker image is created to encapsulate everything for easier running and deployment process.

