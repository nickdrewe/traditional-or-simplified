# traditional-or-simplified
Detect if a string contains Simplified or Traditional Chinese characters.
## Installation & usage
Install `traditional-or-simplified` via NPM:
```sh
npm install traditional-or-simplified
```
In Node:
```js
var TradOrSimp = require('traditional-or-simplified');

// Detect if a string contains Simplified Chinese
TradOrSimp.isSimplified('无需注册或设置')
// True

// Detect if a string contains Simplified Chinese
TradOrSimp.isSimplified('无需注册或设置。')
// True

// Detect if a string contains Traditional Chinese
TradOrSimp.isTraditional('無需帳戶或註冊。')
// True

// Detect if a string contains Traditional or Simplified Chinese characters
TradOrSimp.detect('無需帳戶或註冊。')

{ inputLength: 8, // Length of input string
  simplifiedCharacters: 0, // Count of Simplified Chinese characters
  traditionalCharacters: 4, // Count of Traditional Chinese characters
  detectedCharacters: 'traditional', // Detected character set
  detectionRate: 1 } // Ratio of majority/minority character sets
```
## About
Traditional-or-simplified was built by [Nick Drewe](https://www.twitter.com/nickdrewe) to detect the Chinese character set of pages being published on [publishthis.email](https://www.publishthis.email).
