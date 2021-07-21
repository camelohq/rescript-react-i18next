# Rescript-react-i18next

This is the Rescript version for [i18next/bs-react-i18next](https://github.com/i18next/bs-react-i18next)

## Introduction

Rescript binding for [react-i18next](https://github.com/i18next/react-i18next) components. 

t and Trans components are minimally functional but HOC and Component bindings to provide t to the context 
are not yet available.  If you want to use this in the current state, you need to initialize i18next
in javascript above reason-react and pass t as a parameter.  This is obviously suboptimal so 
if you have reason-react experience, please help improve this starting point!
 
See [bs-ant-design](https://github.com/thangngoc89/bs-ant-design) repo for credit on binding pattern. 

## Installation
```
npm install --save rescript-react-i18next
```

* Add `rescript-react-i18next` to `bs-dependencies` in `bsconfig.json`.


## Usage
```
// pass t down as prop
{t("keyWithValues", Some(Js.Dict.fromList([("placeholder", "value")])))}
{t("keyWithNoInterpolation", None)}

I18next.toString(t("keyForStringParameter", None))

// t will already be in scope if initialized in root of project.
<Trans i18nKey="mykey" values=[("placeholder", "value")] />
```

## Components
t, Trans

## Contributions

All contributions are welcomed.  I intend to merge and release anything you pull request quickly.

## TODO
- [bs-react-intl](https://github.com/alexfedoseev/bs-react-intl) has similar bindings to learn from potentially as examples
of how to extend functionality here.
- HOC and Component 
- figure out how to not have to pass None to t if there are no values

## LICENSE

MIT
