
#### LOG:

  ```
  ssh dokku@{{dominio}} logs {{subdominio}}
  ```



#### VARIABLES DE ENTORNO:

  SET:
    ```
    ssh dokku@{{dominio}} config:set {{subdominio}} VARIABLE1='value' VARIABLE2='value'
    ```
  GET:
    ```
    ssh dokku@{{dominio}} config {{subdominio}} vars
    ```



#### RESET:

  ```
  ssh dokku@{{dominio}} ps:restart {{subdominio}}
  ```



#### BUILDEAR A MANO:
  ```
  git push {{ambiente}} dev:master
  ```

  

#### OTROS:

  ```
  NODE_ENV={{ambiente}} node .
  ```
