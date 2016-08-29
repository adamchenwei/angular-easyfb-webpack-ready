# angular-easyfb-webpack-ready
A webpack ready version of the angular-easyfb

# Usage
ensure angular and webpack are properly setup in your environment. Then simple `clone` this report into your source and BOOM! Its ready to use!

# Example

lets say you put the easyfb in your `src/easyfb` folder, meanwhile you have angular component needs to use it is located in another folder in the `src`, like, `src/mycomponent`, then all you need to do is the following to initiate the setup for it:

````
import angular from 'angular';
import easyfacebook from './../easyfacebook/easyfacebook';

let myComponentModule = angular.module('theAppModuleItself', [
  easyfacebook.name,
])

.config((ezfbProvider) => {
  ezfbProvider.setInitParams({
    appId: '0101010101001', //your app id
    version: 'v2.5'
  });

})
.component('myComponent', theAppModuleItself)

export default myComponentModule;

````
