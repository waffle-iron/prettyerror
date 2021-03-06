[![Stories in Ready](https://badge.waffle.io/erremauro/prettyerror.png?label=ready&title=Ready)](https://waffle.io/erremauro/prettyerror)
# PrettyError

A simple javascript class to print meaningful errors, inspired by [elm][1]'s error verbosity.

![PrettyError screenshot][2]

[1]: http://elm-lang.org
[2]: screenshot/screenshot.png


## Installation

Add PrettyError to your project from github:

```bash
npm install git+https://github.com/erremauro/prettyerror.git
```


## Wait, no NPM?

This is stupid and shouldn't "bloat" NPM with its kb.


## How to use it.

```javascript
import { createError, logError } from 'pretty-error'

const errProps = {
  code: -1,
  name: 'PathNotFound',
  filepath: dirPath,
  describe: 'Required directory is missing from current path.'
  explain: 'The application was expecting to find a directory at path: '
    + dirPath + ' but none was found. Please verify your current path.'
  example: 'To verify your current path type "pwd" in your terminal window'
}

let prettyError = create( 'Path not found', errProps )
logError( prettyError )
```


`createError` will create a new `PrettyError` object instance, while `logError`
will log your error to the console. 

You can also work directly with `PrettyError` ( for example if you whish to `extend` it ) by importing the class directly from the module with: `import { PrettyError } from 'pretty-error'`


## CREDITS

2016, Roberto Mauro


## LICENSE

Really?
