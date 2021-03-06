# couponjs
This is a simple coupon creation project using NodeJS.

[![license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/yusufshakeel/couponjs)
[![npm version](https://img.shields.io/badge/npm-0.3.0-blue.svg)](https://www.npmjs.com/package/couponjs)
[![Build Status](https://travis-ci.com/yusufshakeel/couponjs.svg?branch=master)](https://travis-ci.com/yusufshakeel/couponjs)

# Getting Started
Add this to your project using npm.
```
> npm i couponjs
```

## Tests
Test code of this project is inside the `tests` directory.

Using the following for testing:
* Jest

## Generate coupon
Create an object of Coupon.
```javascript
const Coupon = require('couponjs');

const coupon = new Coupon();
```

Now, call the `generate` method.
```javascript
const myCoupon = coupon.generate();
```

By default, `generate` will return coupon code of length 6 using uppercase alphabet.

### Coupon of length N
To generate coupon of a given length we pass the following option to the `generate` method.
```javascript
const myCoupon = coupon.generate({
  length: 8
});
```
Where, 8 in the above code represent the total number of characters that will be present in the coupon.

Range of `length`:
* Min: 1
* Max: 128

If length is not passed then default value of 6 is considered.

### Coupon with prefix
To generate a coupon with a given prefix we pass the following option to the `generate` method.
```javascript
const myCoupon = coupon.generate({
  prefix: 'SUPER'
});
```
The above code will generate coupon with prefix 'SUPER'. Default lenght of the coupon is 6. So, we will get coupon like the following.

`SUPERAAAAAA`

Note! Prefix characters are not counted.

If we want to generate coupon of length 3 with prefix 'SUPER' then our option will look like the following.
```javascript
const myCoupon = coupon.generate({
  length: 3,
  prefix: 'SUPER'
});
```
We will get coupon like the following `SUPERAAA`.

### Coupon with suffix
To create coupon with suffix pass the following option.
```javascript
const myCoupon = coupon.generate({
  length: 3,
  suffix: 'AWESOME'
});
```
The above code will generate coupon like the following `ZZZAWESOME`.

Note! Characters of the suffix is not counted. If length is note specified then default value of 6 is considered as the length.

### Coupon with prefix and suffix
To create coupon with prefix and suffix pass the following option.
```javascript
const myCoupon = coupon.generate({
  length: 6,
  prefix: 'SUPER',
  suffix: 'AWESOME'
});
```
The above code will generate coupon like the following `SUPERZZZZZZAWESOME`.

Note! The characters of the prefix and suffix is not considered. If length is not specified then default value of 6 is considered.

## License
It's free :smiley:

[MIT License](https://github.com/yusufshakeel/couponjs/blob/master/LICENSE) Copyright (c) 2020 Yusuf Shakeel

### Back this project

If you find this project useful and interesting then feel free to support it on [Patreon](https://www.patreon.com/yusufshakeel).

### Donate
Feeling generous :smiley: [Donate via PayPal](https://www.paypal.me/yusufshakeel)