Smalltalk [![License][LicenseIMGURL]][LicenseURL] [![NPM version][NPMIMGURL]][NPMURL] [![Dependency Status][DependencyStatusIMGURL]][DependencyStatusURL] [![Build Status][BuildStatusIMGURL]][BuildStatusURL]
====
_Modified for N1_

**You must change the `nylas://` link in `smalltalk.css` for this to work in plugins.**
**In addition, you must copy `smalltalk.css` to your plugin's `stylesheets` directory.**


Simple [Promise](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Promise)-based replacement of native Alert, Confirm and Prompt.

# Install
With help of npm:

```
npm i git+https://github.com/mbilker/smalltalk.git
```

# API

In every method of `smalltalk` last parameter *options* is optional and could be used
for preventing of handling cancel event.

```js
{
    cancel: true /* default */
}
```

## smalltalk.alert(title, message [, options])

![Alert](https://raw.githubusercontent.com/mbilker/smalltalk/master/screen/alert.png "Alert")

```js
smalltalk.alert('Error', 'There was an error!').then(function() {
  console.log('ok');
}, function() {
  console.log('cancel');
});
```

## smalltalk.confirm(title, message [, options])

![Confirm](https://raw.githubusercontent.com/mbilker/smalltalk/master/screen/confirm.png "Confirm")

```js
smalltalk.confirm('Question', 'Are you sure?').then(function() {
  console.log('yes');
}, function() {
  console.log('no');
});
```

## smalltalk.prompt(title, message, value [, options])

![Prompt](https://raw.githubusercontent.com/mbilker/smalltalk/master/screen/prompt.png "Prompt")

```js
smalltalk.prompt('Question', 'How old are you?', '10').then(function(value) {
  console.log(value);
}, function() {
  console.log('cancel');
});
```

#License
MIT

[NPMIMGURL]:                https://img.shields.io/npm/v/smalltalk.svg?style=flat
[BuildStatusIMGURL]:        https://img.shields.io/travis/mbilker/smalltalk/master.svg?style=flat
[DependencyStatusIMGURL]:   https://img.shields.io/gemnasium/mbilker/smalltalk.svg?style=flat
[LicenseIMGURL]:            https://img.shields.io/badge/license-MIT-317BF9.svg?style=flat
[NPMURL]:                   https://npmjs.org/package/smalltalk "npm"
[BuildStatusURL]:           https://travis-ci.org/mbilker/smalltalk  "Build Status"
[DependencyStatusURL]:      https://gemnasium.com/mbilker/smalltalk "Dependency Status"
[LicenseURL]:               https://tldrlegal.com/license/mit-license "MIT License"
