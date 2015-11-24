# cepdb-js
Javascript plugin for cepdb api (https://github.com/lfreneda/cepdb)

## How to install

- Install it with [bower](http://bower.io/)

```javascript
    bower install cepdb-js
```

- Add a script a tag for `cepdb-js/index.js`

```html
    <script src="/bower_components/cepdb-js/index.js"></script>
```

## How to use

```javascript
    var cepDb = new CepDb();

    cepDb.search('05422010', {
        onSuccess: function(data) {
            alert(JSON.stringify(data));
        },
        onTimeout: function() {
            alert('timed out :(');
        }
    });
```

## API
 
 search( **string** `cep`, **object** `options` )
 
 * **cep** `cep` - cep to be searched
 * **object** `options` - global upload options
   * **function** `onSuccess` - callback to be called on success 
   * **function** `onTimeout` - callback to be called on request timed out 
   * **int** `timeout` - remove thumbnail versions after sucessful upload (**default**: `10`)


#### Working Sample
 
 - clone this repository and browse [examples/index.html](https://github.com/lfreneda/cepdb-js/blob/master/examples/index.html) :)   
