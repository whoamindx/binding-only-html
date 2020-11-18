# binding-only-html

> 100kb of frameworks and javascript libraries? No more, HTML is power (oh yeah 🤘)

## See how simple it is

Do you think you really need a 1 TB framework to make a simple binding? Keep reading and I'll show you how to do this with just two lines of HTML.
THAT'S IT! 2 FUCKED LINES OF HTML.

First, see a comparison with the famous jQuery(or John Query for the most intimate) and AngularJS:

## With jQuery

``` html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Binding with jQuery</title>

    <script src="https://code.jquery.com/jquery-3.3.1.min.js" integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8=" crossorigin="anonymous"></script>
    <script>
      $(() => {
        const message = $('#message')
        const demo = $('#demo')

        message.keyup(() => {
          demo.text(message.val())
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

Big, don't you think?

## With AngularJS

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

Simple isn't it? But are you really going to load 165 KB of JavaScript just to do that?

## ONLY 2 LINES OF HTML

``` html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Binding Only HTML</title>
  </head>
  <body>
    <input type="text" oninput="demo.innerHTML = this.value">
    <p id="demo"></p>
  </body>
</html>
```

Did you like it? Simple right, you can still transform it into a "two-way" binding simply with the addition of 2 attributes and a fucking ID.

``` html
<input type="text" id="message" oninput="demo.innerHTML = this.value">
<p id="demo" contenteditable oninput="message.value = this.innerHTML"></p>
```

## Attention ⚠️
Obviously, this is just a joke, don't take it seriously. 👾
