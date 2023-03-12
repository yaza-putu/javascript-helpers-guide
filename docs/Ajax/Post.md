# Post
You can use this method for reusable code jquery ajax request with method POST
> For Laravel you need paste bellow in main head for auto send csrf
```html
<meta name="csrf-token" content="{{ csrf_token() }}">
```

### You can choose one type notification error
- 'sweetError'
- 'toastError'
- 'snackbarError'
- 'snackbar'

> Note : if you use laravel and use FormRequest to handle validation, key from array error data if same with input name it auto show validation error to html

### Expectation response error data
```json
{
  "errors": {
    "nama": [
      [
        "Nama wajib diisi"
      ]
    ],
    "email": [
      [
        "Email wajib diisi"
      ]
    ],
  }
}
```
example :
- your input form
```html
<form method="post">
    <input type="text" name="email">
</form>
```
- auto handel validation form if call ajaxPost() or manual call handleValidation()
- result like

![result](/img/error-validation.png)
- more doc [Click here](https://gist.github.com/yaza-putu/0e8c13100e1ef9f29306c8c4ef07d3c1)

## Post only data
> Method name : ajaxPost(url , data, button = null, typeErrorNotification = 'sweetError') 

### Parameter
- url (string)
- data (Generate from new FormData())
- button (string) id or class element like '#button' or '.button' for auto insert or delete loading animation

### How to call
- basic
```javascript
ajaxPost('http://localhost/post-data', {}, '#button-submit')
    .done(function (res){
        // write more action if success
    })
```
- with error handel or always 
```javascript
ajaxPost('http://localhost/post-data', {}, '#button-submit')
    .done(function (res){
        // write more action if success
    })
    .fail(function (res){
        // write more action if error
    })
    .always(function (res){
        // write more action auto run end of request
    })
```
- with choose error notification 
```javascript
ajaxPost('http://localhost/post-data', {}, '#button-submit', 'sweetError')
    .done(function (res){
        // write more action if success
    })
```

## Post File With Progress Bar
> Method name : ajaxPostFile(url, data, button = null, showLoading = '#loading-body')

![progress](https://dyclassroom.com/image/topic/bootstrap/progress-bar/contextual-progress-bar.png)

This method auto capture your progress upload from 0% to 100%, good use form upload file

### Parameter
- url (string)
- data (Generate from new FormData())
- button (string) like '#button' or '.button' for auto show hide loading animation
- showLoading (string) where you show loading bar ex : '#result'

### How to call
- basic
```html
<div id="loading-progress"></div>
```
```javascript
ajaxPostFile('http://localhost/upload-file', {}, '#btn-submit', '#loading-progress')
    .done(function (res){
        // write more action
    })
```
- with handel error or always
```javascript
ajaxPostFile('http://localhost/upload-file', {}, '#btn-submit', '#loading-progress')
    .done(function (res){
        // write more action
    })
    .fail(function (res){
        // write more action
    })
    .always(function (res){
        // write more action
    })
```