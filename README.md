# dependency-badger
Provides markdown compatible badges for project dependencies

## Examples
 - a standard badge example from `shields.io` using normal markdown [![node](https://img.shields.io/badge/node_version-6.0.0-blue.svg?style=flat&maxAge=2592000)](https://nodejs.org/dist/latest-v6.x/docs/api/)
    ```md
    [![node](https://img.shields.io/badge/node_version-6.0.0-blue.svg?style=flat&maxAge=2592000)](https://nodejs.org/dist/latest-v6.x/docs/api/)
    ```
 - a dynamic example from the main dependency list (short form) [![express](https://dependency-badger-robinknpie.c9users.io/badge/?d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)]()
    ```md
    [![express](https://dependency-badger-robinknpie.c9users.io/badge/?d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)]()
    ```
 - a dynamic example from the main dependency list (full form) [![express](https://dependency-badger-robinknpie.c9users.io/badge/?dependency=express&colour=blue&img_type=svg&badge_style=flat&dependency_type=dependencies&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)]()
    ```md
    [![express](https://dependency-badger-robinknpie.c9users.io/badge/?dependency=express&colour=blue&img_type=svg&badge_style=flat&dependency_type=dependencies&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)]()
    ```
 - a dynamic example from the dev dependency list (short form) [![mocha](https://dependency-badger-robinknpie.c9users.io/badge/?d=mocha&t=devDependencies&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)]()
    ```md
    [![mocha](https://dependency-badger-robinknpie.c9users.io/badge/?d=mocha&t=devDependencies&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)]()
    ```
 - a dynamic example from the dev dependency list (full form) [![mocha](https://dependency-badger-robinknpie.c9users.io/badge/?dependency=mocha&colour=blue&img_type=svg&badge_style=flat&dependency_type=devDependencies&package_path=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)]()
    ```md
    [![mocha](https://dependency-badger-robinknpie.c9users.io/badge/?dependency=mocha&colour=blue&img_type=svg&badge_style=flat&dependency_type=devDependencies&package_path=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)]()
    ```

## Badge generation
There are a 2 mandatory parameters need to generate a badge:
 - **d**, **dependency** - this must match one of the dependencies in your project's `package.json` file
 - **p**, **package_path** - this is the URL to the raw form of your project's `package.json` file
```md
https://dependency-badger-robinknpie.c9users.io/badge/?d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
https://dependency-badger-robinknpie.c9users.io/badge/?dependency=express&package_path=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
```
There are also some optional parameters that can be used to customise the returned badge:
 - **t**, **dependency_type** - this allows for badge creation for dependencies defined outside of the _main_ `dependencies` section, and MUST be specified if the dependency is not in the main section
    ```md
    https://dependency-badger-robinknpie.c9users.io/badge/?t=devDependencies&d=mocha&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
    https://dependency-badger-robinknpie.c9users.io/badge/?dependency_type=devDependencies&d=mocha&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
    ```
 - **c**, **colour** - this is `blue` by default and governs the background colourof the version number part of the badge
 - **s**, **badge_style** - this is `flat` by default and changes the styling of the badge, the possible values are:
     - `flat` ![flat](https://dependency-badger-robinknpie.c9users.io/badge/?s=flat&d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)
        ```url
        https://dependency-badger-robinknpie.c9users.io/badge/?s=flat&d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
        https://dependency-badger-robinknpie.c9users.io/badge/?badge_style=flat&dependency=express&package_path=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
        ```
     - `flat-square` ![flat-square](https://dependency-badger-robinknpie.c9users.io/badge/?s=flat-square&d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)
        ```url
        https://dependency-badger-robinknpie.c9users.io/badge/?s=flat-square&d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
        https://dependency-badger-robinknpie.c9users.io/badge/?badge_style=flat-square&dependency=express&package_path=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
        ```
     - `plastic` ![plastic](https://dependency-badger-robinknpie.c9users.io/badge/?s=plastic&d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)
        ```url
        https://dependency-badger-robinknpie.c9users.io/badge/?s=plastic&d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
        https://dependency-badger-robinknpie.c9users.io/badge/?badge_style=plastic&dependency=express&package_path=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
        ```
     - `social` ![social](https://dependency-badger-robinknpie.c9users.io/badge/?s=social&d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json)
        ```url
        https://dependency-badger-robinknpie.c9users.io/badge/?s=social&d=express&p=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
        https://dependency-badger-robinknpie.c9users.io/badge/?badge_style=social&dependency=express&package_path=https://raw.githubusercontent.com/RobinKnipe/dependency-badger/master/package.json
        ```
