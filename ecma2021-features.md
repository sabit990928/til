# ECMAScript 2021 features

_Background:_ I listened [Фронтенд Юность](https://apple.co/3nEOdbV) podcast which was recorded before NY and at some point they discussed about what was new in JS previous year. I found some new, helpful myself too.

Logical assignment operators. It's pretty helpful command and has 3 varieties: And & Equals (&&=), OR & Equals (||=), Nullish coalescing & Equals (??=). 

```javascript
// &&=
let x = 1;
x &&= 10;
// x will be 10

// ||=
let x = 0;
x ||= 9
// x will be 9

// ??=
let x;
let y = 10;
x ??= y;
// both x and y will be 10, because x was undefined
```

There was some other new stuff and private class methods was new for me. You can check other updates by [this](https://www.geeksforgeeks.org/new-features-in-ecmascript-2021-update/) link.