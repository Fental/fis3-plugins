## usage

```
// fis-conf.js

var stylelintConf = {};

fis.match('*.{css,scss,less,sss}}', {
  lint: fis.plugin('stylelint', stylelintConf)
});
```

### options

```
var stylelintConf = {
  fix: , // ❗!!! important !!!❗
         // this is not part of stylelint
         // default:false,
         // be careful, this might change your source code
         // if this set to true, linter will try to fix code using `stylefmt`
         // and also notice  `stylefmt` is not currently full compatible with `stylelint`
         // eg: `value-list-comma-newline-after` it not supported by `stylefmt`
         // `stylefmt` will combine value list in to one line,
         // and `stylelint` will report a error,
         // also this might againt the `max-line-length` rule
  code: // useless, will be unset
  codeFilename: // useless, will be unset
  config:
  configBasedir:
  configFile:
  configOverrides:
  files: // useless, will be overwrite
  formatter: // useless, will be overwrite
  ignorePath:
  syntax: // if not set, will fix by file ext
          // rules: .scss => scss, .less => less, .sss =>sugarss
};
```
options: [http://stylelint.io/user-guide/node-api/#options]

rules: [http://stylelint.io/user-guide/rules/]
