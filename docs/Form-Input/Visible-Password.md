# Visible Password
> Method Name : visiblePassword(elementTrigger, elementVisible)

### Parameter
- elementTrigger (string) => id or class element trigger click like '#btn-show-password'
- elementVisible (string) => id or class element to change type input from password to text 

### How to call
- basic
```html
<button id="btn-show-password">Show password</button>
<input type="password" id="password">
```
```javascript
visiblePassword('#btn-show-password', '#password')
```