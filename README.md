# loggedin-mixin


## Install

```sh
$ meteor add tunifight:loggedin-mixin
```

## Usage

```js
// Method definition
const method = new ValidatedMethod({
  name, // DDP method name
  mixins : [LoggedInMixin],
  checkLoggedInError: {
    error: 'notLogged',
    message: 'You need to be logged in to call this method',//Optional
    reason: 'You need to login' //Optional
  },
  validate, // argument validation
  run // Method body
});
```

The LoggedInMixin mixin requires the new `checkLoggedInError` option which includes
the required informations to throw an Error. Note that `message` and `reason` are optional.
