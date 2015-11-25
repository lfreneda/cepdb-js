# cepdb-js
Javascript plugin para cepdb api (https://github.com/lfreneda/cepdb)

## Instalação

- Instalação com [bower](http://bower.io/)

```javascript
    bower install cepdb-js
```

- Adicione uma tag script para o arquivo `cepdb-js/index.js`

```html
    <script src="/bower_components/cepdb-js/index.js"></script>
```

## Uso

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
 
 * **cep** `cep` - cep que deseja resolver
 * **object** `options` - objeto de opções para chamada 
   * **function** `onSuccess` - callback que será invocada em caso de sucesso.
   * **function** `onTimeout` - callback que será invocada em caso de timeout.
   * **int** `timeout` - tempo de espera da requisição (em segundos) (**default**: `10`)


#### Exemplo
 
 - clone o repositorio e abra o seguinte arquivo no seu browser preferido: [examples/index.html](https://github.com/lfreneda/cepdb-js/blob/master/examples/index.html) :)   
