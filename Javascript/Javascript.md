# Javascript

### Variáveis

- var

- let

- const

  <img src="C:\Users\Casa\AppData\Roaming\Typora\typora-user-images\image-20220626161729197.png" alt="image-20220626161729197" style="zoom:70%;" />

### Tipos

- Strings

- Numbers

- Booleans

- Arrays

- Objetos 

  ```js
  let person = {
      name: 'John',  	//name and age are Keys
      age: 20		 	//'John' and 20 are values
  }
  ```

- Null, 



#### Funções

- **Estrutura da função**

  ```js
  function nome(parametros){
      //instruções
      return; //Para a função e pode retornar um valor
  }
  ```

- **Função Anônima** (Não possui nome)

- **Função autoinvocável** (IIFE: Immediately Invoked Function Expression)

  ```js
  (
      function(a, b) {
          return a + b;
      }
  )(1, 2); //(); indica que ela é autoinvocável.
  ```

- **Callbacks** (Função passada como argumento para outra função)

```js
const calc = function(operacao, num1, num2){
    return operacao(num1, num2);
}...
```



#### Parâmetros

- Arguments (Mostra todos os parâmetros carregados em uma função)

- Arrays: 

  - Técnica do Spread (lidar com argumentos de um array separadamente)

  ```js
  function sum(x, y, z){
      return x + y + z;
  }
  const numbers = [1, 2, 3];
  console.log(sum(...numbers)); //... transforma cada argumento do array em um elemento independete
  ```

  - Técnica do Rest (combinar os elementos em um array)

    ```js
    function confereTamanho(...args){
        console.log(args.length)
    }
    confereTamanho(3, 4, 5) //tamanho será 3.
    ```

- Objetos

  - Object Destructuring (filtrar os dados em um objeto)

    ```js
    const user = {
        id: 42;
        firstName: 'Adriano'
        lastName: 'Aguiar'
    }
    function userId({id}){ //usar {} para selecionar um dado do objeto.
        return id;
    }
    userId(user) //retorna somente 42.
    ```



#### Condições

- if e else. Obs.: (else if) é separado em Javascript

- switch: Sempre tem um default

  ```js
  switch(id){
      case 1:
          return 1;
      case 2:
          return 2;
      default:
          return 0;
  }
  ```

- for: Loop

  - **Tradicional**

    ```js
    for (let i = 0; i < 10; i++){
        
    }
    ```

  - **for in**: Loop entre propriedades enumeráveis de objeto

    ```js
    function forInExemplo(obj){
        for(prop in obj){
            console.log(obj[prop]);
        }
    }
    const meuObjeto = {
        nome: "João",
        idade: "20",
        cidade: "Salvador"
    }
    forInExemplo(meuObjeto); // retorna no console João, 20, Salvador 
    ```

  - **for on**: Loop entre estruturas iteráveis (arrays, strings)

    ```js
    function logLetras(palavra) {
        for(letra of palavra){
            console.log(letra);
        }
    }
    const palavra = "abacaxi";
    logLetras(palavra)
    //a
    //b
    //...
    //i
    ```

- **while:** Executa instruções até que a condição se torne falsa

- **do while:** Faz o mesmo que o while, mas a primeira execução sempre ocorre.

  ```js
  function exemploDoWhile(){
      let num = 6;
      do{
          console.log(num);
          num++;
      } while(num <= 6)
  }
  exemploDoWhile() //retorna somente 6
  ```

- **this:** referência para o contexto 

![image-20220626201929489](C:\Users\Casa\AppData\Roaming\Typora\typora-user-images\image-20220626201929489.png)

- Manipulando o valor de **this**

  - call

    ```js
    const myObj = {
        num1: 2;
        num2: 4;
    };
    function soma(a,b){
        console.log(this.num1 + this.num2 + a + b);
    }
    soma.call(myObj, 1, 5);
    ```

  - Apply

    ```js
    const myObj = {
        num1: 2;
        num2: 4;
    };
    function soma(a,b){
        console.log(this.num1 + this.num2 + a + b);
    }
    soma.call(myObj, [1, 5]); //diferença entre o call é que os argumentos vão em uma array.
    ```



#### Arrow functions

- Sintaxe

  ```js
  const helloWorld = () => {
      return "Hello World";
  }
  
  const helloWorld = () => "Hello World"; //não precisa do return e nem das chaves quando é feito em uma linha.
  ```

- Arrow function não faz hoisting. (Ela deve ser declarada antes de ser chamada).
- "this" é sempre global na arrow function
- Não existe o objeto "arguments"
