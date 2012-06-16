# Shelley

Shelley is a view selector engine which can be plugged in to [Frank](http://www.testingwithfrank.com). It is Frank's default selector engine.

Shelley aims to be backwards compatible with the UIScript selector syntax, which is part of UISpec. Details about this UIScript syntax can be found in [UISpec's documentation](http://code.google.com/p/uispec/wiki/Documentation#UIScript).

## Differences from UIScript

The UIScript system that Shelley replaces allowed you to select views and also perform operations against those views within the same query. For example in UIScript you would do something like `view marked:'foo' touch`. Shelley is intended to be used solely as a view selection mechanism. The operation you would like to be performed is specified seperately from the Shelley selector string. So instead of performing the touch right in the query you would do something like `frankly_map( "view marked:'touch'", 'touch' )` in your ruby test script.

## Alternative Selector Engines

Frank exposes a plugin system which lets you use alternative selector engines beyond Shelley. Some options for alternative engines are:

- [Igor](https://github.com/dhemery/igor), which provides CSS-like selectors
- [ValueAddKeyPath](https://github.com/KingOfBrian/ValueAddKeyPath), which is based on key paths and NSPredicate
- [SelectorKit](https://github.com/soutaro/SelectorKit), another CSS-like approach
###License

Copyright 2012 ThoughtWorks, Inc. Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0 Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
