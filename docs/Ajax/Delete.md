# Delete
![delete confirm](https://i.stack.imgur.com/vTszi.png)

You can use this function to auto handel delete data with pop up confirmation from sweetalert2
> Method name : ajaxDelete(url, id,reload = false,typeNotification = 'sweetSuccess', table = null, confirmSweetDelete = null)

> Note : only method post not use method get right

### Available more type notification success
- 'sweetSuccess'
- 'notifySuccess'
- 'toastSuccess'
- 'snackbarSuccess'

### Parameter
- url (string)
- id (primary key of data)
- reload (boolean) => reload page after success or no
- typeNotification (string) => choose one success notification
- table (string|null) => if use datatable you can call id or class from element table for handel auto refresh table (only for datatables)
- confirmSweetDelete (json|null) => custom delete confirmation message

### How To Call
- basic
```javascript
ajaxDelete('http://localhost/delete', 'idPrimaryKey')
```
- with auto reload page after done delete data
```javascript
ajaxDelete('http://localhost/delete', 'idPrimaryKey', true)
```
- with custom notification success
```javascript
ajaxDelete('http://localhost/delete', 'idPrimaryKey', false, 'sweetSuccess')
```
- with auto reload table (datatables plugin)
```javascript
ajaxDelete('http://localhost/delete', 'idPrimaryKey', false, 'sweetSuccess')
```
- with custom confirmation message
```javascript
const confirmSweetDelete = {
    title : 'Are you sure?',
    body : 'The data will be deleted and cannot be recovered!',
    buttonLabel : 'Delete',
    buttonConfirmColor : "#6c5ce7",
}
```
```javascript
ajaxDelete('http://localhost/delete', 'idPrimaryKey', false, 'sweetSuccess', null,confirmSweetDelete)
```