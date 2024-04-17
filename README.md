# lite-breakpoints
[![npm](https://img.shields.io/npm/v/lite-breakpoints)](https://www.npmjs.com/package/lite-breakpoints)

This is a very small and lightweight library that simplifies working with media queries to create adaptability on the site. 

## Install
* To work with this library, you will need to install **sass** in your project (obviously):
	```sh
	npm install sass -D
	```
* To install the library, run this command:
	```sh
	npm install lite-breakpoints -D
	```

## Usage
**WARNING**: You need to initialize the global variable **$lite-variables** in order to set breakpoints for your project. After that, you need to import the library itself into a scss file.
```scss
$lite-breakpoints:(xs: 0,
  sm: 375px,
  md: 560px,
  lg: 900px,
  xl: 1200px,
  xxl: 1400px);
  
@import "~lite-breakpoints";
```
That's all! Now you can use convenient mixins for adaptivity in your projects. Good luck!
```scss
.text {
  @include breakpoint-up(lg) {
    color: red;
  }
}
.container {
  @include breakpoint-down(xl) {
    width: 200px;
  }
}
```
