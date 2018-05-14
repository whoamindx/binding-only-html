# binding-somente-html

> 100kb de frameworks e bibliotecas javascript? Não mais, HTML é poder (oh yeah 🤘)

## Veja como é simples

Você acha que precisa mesmo de um framework de 1 TB para fazer um simples binding? Continue lendo e mostrarei como fazer isso com apenas duas linhas de HTML.
ISSO MESMO, 2 LINHAS DE HTML DO CARALHO.

Primeiro, veja uma comparação com o nosso famoso jQuery (ou JoãoQuery para os mais íntimos) e AngularJS:

## Com jQuery

``` html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Binding with jQuery</title>

    <script src="https://code.jquery.com/jquery-3.3.1.min.js" integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8=" crossorigin="anonymous"></script>
    <script>
      $(()=>{
        let message = $('#message');
        let demo = $('#demo');

        message.keyup(()=>{
          demo.text(message.val());
        })
      })
    </script>
  </head>
  <body>
    <input type="text" id="message">
    <p id="demo"></p>
  </body>
</html>
```

Grande você não acha?

## Com AngularJS

``` html
<!DOCTYPE html>
<html ng-app>
  <head>
    <meta charset="UTF-8">
    <title>Binding with AngularJS</title>

    <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
  </head>
  <body>
    <input type="text" ng-model="message">
    <p>{{message}}</p>
  </body>
</html>
```

Simples não é? Mas você vai mesmo carregar 165 KB de JavaScript só para fazer isso?

## APENAS 2 LINHAS DE HTML

``` html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Binding Only HTML</title>
  </head>
  <body>
    <input type="text" oninput="demo.innerHTML=this.value;">
    <p id="demo"></p>
  </body>
</html>
```

Curtiu? Simples né, você ainda pode transformar em um "two-way" binding simplesmente com a adição de 2 atributos e um ID porra.

``` html
<input type="text" id="message" oninput="demo.innerHTML=this.value;">
<p id="demo" contenteditable oninput="message.value=this.innerHTML;"></p>
```

## Atenção ⚠️
Obviamente, isso é apenas uma piada, não leve a sério. 👾
