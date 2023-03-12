# Get
This method handel ajax get request
> Method name : ajaxGet(url, blockUi = false)

### Parameter
- url (string)
- blockUi (boolean) => to enable disable block ui screen

### How to call
- basic
```javascript
ajaxGet('http://localhost/data')
    .done(function (res){
        // write more action
    })
```
- with handel error or always
```javascript
ajaxGet('http://localhost/data')
    .done(function (res){
        // write more action
    })
    .fail(function (res){
        // write more action
    })
    .always(function (){
        // write more action
    })
```
- auto block screen
```javascript
ajaxGet('http://localhost/data', true)
    .done(function (res){
        // write more action
    })
```

result like

![block ui](https://jquery-plugins.net/image/plugin/jquery-blockui-plugin.jpg)