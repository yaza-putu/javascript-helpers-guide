# Datatables
You can call datatables function to connect with yajra datatables to handel big data
> Method name : datatable(table, url, columns= [], columnDefs = [], callback, responsive = true)

### Parameter
- table (string) => id or class element table like '#table'
- column (array) => column setting
- columnDefs (array) => column setting
- callback (function) => you can implementation function like filter or etc
- responsive (boolean) => responsive in mobile view yes or no

### How To Call
- basic
```javascript
  let columns = [
        {data: 'DT_RowIndex', name: 'DT_RowIndex', width: '10px', orderable: false, searchable: false},
        {data: 'name', name: 'name'},
        {data: 'image', name: 'image'},
        {data: 'opsi', name: 'opsi', orderable: false, searchable: false},
    ];
    // config columnDefs
    let columnDefs = [
        {responsivePriority: 1, targets: 0},
        {responsivePriority: 2, targets: 1},
        {responsivePriority: 3, targets: 3},
        {responsivePriority: 4, targets: 2},
    ];
    // set url
    let url = $('#table-url').val();
    // set tableId
    let table = '#table';  
```
```javascript
datatable(table, url, columns, columnDefs);
```
- with filter function
```javascript
  let columns = [
        {data: 'DT_RowIndex', name: 'DT_RowIndex', width: '10px', orderable: false, searchable: false},
        {data: 'name', name: 'name'},
        {data: 'image', name: 'image'},
        {data: 'opsi', name: 'opsi', orderable: false, searchable: false},
    ];
    // config columnDefs
    let columnDefs = [
        {responsivePriority: 1, targets: 0},
        {responsivePriority: 2, targets: 1},
        {responsivePriority: 3, targets: 3},
        {responsivePriority: 4, targets: 2},
    ];
    // set url
    let url = $('#table-url').val();
    // set tableId
    let table = '#table';  
```
```javascript
function filter(d){
    d.paramKey = 'valueFilter';
}
```
```javascript
datatable(table, url, columns, columnDefs, filter);
```
- with mobile responsive
```javascript
  let columns = [
        {data: 'DT_RowIndex', name: 'DT_RowIndex', width: '10px', orderable: false, searchable: false},
        {data: 'name', name: 'name'},
        {data: 'image', name: 'image'},
        {data: 'opsi', name: 'opsi', orderable: false, searchable: false},
    ];
    // config columnDefs
    let columnDefs = [
        {responsivePriority: 1, targets: 0},
        {responsivePriority: 2, targets: 1},
        {responsivePriority: 3, targets: 3},
        {responsivePriority: 4, targets: 2},
    ];
    // set url
    let url = $('#table-url').val();
    // set tableId
    let table = '#table';  
```
```javascript
datatable(table, url, columns, columnDefs, function (){}, true);
```