# Browser Support for CSS / SCSS
Browser support let you use simple SCSS mixins to apply code only for a specific browser. This can be handy in case you want to write your fallback code specific for Internet Exployer 11. 

## Currently Supports:
- Internet Exployer 11

## How to use
```scss 
	@include browser(IE11){
		// your specific code for IE11 here
	}
```

## Example
### SCSS Code
```scss
.myClass::before {
	@include browser(IE11){
		content: 'IE11 only';
	}   
}
```

### CSS Outputs
```css
@media all and (-ms-high-contrast: none), (-ms-high-contrast: active) {
	*::-ms-backdrop, .myClass::before {
		content: 'IE11 only';
	}
}
```