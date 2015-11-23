# cepdb-js
Javascript plugin for cepdb api (https://github.com/lfreneda/cepdb)

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

### API
 
 search( **string** `cep`, **object** `options` )
 
 * **cep** `cep` - cep to be searched
 * **object** `options` - global upload options
   * **function** `onSuccess` - callback to be called on success 
   * **function** `onTimeout` - callback to be called on request timed out 
   * **int** `timeout` - remove thumbnail versions after sucessful upload (**default**: `10`)
