# Conceitos básicos - Oficina de introdução à linguagem PHP

Nesta parte conheceremos os conceitos mais básicos da linguagem (variáveis, tipos, operadores e erros).
Para isso utilizaremos o interpretador interativo (ext-readline), executando o comando abaixo:

```sh
php -a
```

## Variáveis

- Escopo
- Variáveis variáveis

```php
<?php

$testing = 'blah'; // Escopo global
var_dump($_SERVER); // Escopo superglobal

$blah = 'Uhull!';

echo $$testing; // Variável variável, saída será: Uhull!
```

## Tipos básicos

```php
<?php
// boolean
$testing = true;
$testing = false;

// integer
$testing = 10;

// float
$testing = 5.4;

// string
$testing = "one";
$testing = 'other';

// array
$testing = [1, 2, 3, 'a', 'b', 'c'];
$testing = ['one' => 1];
$testing = array(1, 2, 3, 'a', 'b', 'c');
$testing = array('one' => 1);

// NULL
$testing = null;
```

## Operadores básicos

Bem parecido com Java, exceto:

- ```-$x```: negação aritimética
- ```**```: exponenciação
- ```===```: comparação identica
- ```!==```: comparação não identica
- ```.```: concatenação

## Type juggling (black magic! :smile:)

```php
$testing = "0"; // string
$testing = $testing + 2; // Agora é int
$testing = $testing + 0.5; // Vixe, float

var_dump(true == 1); // true
var_dump(true === 1); // false

var_dump(true == "true"); // true
var_dump(true === "true"); // false

var_dump(10 == "10"); // true
var_dump(10 === "10"); // false
```

## Erros básicos

- Parse error
- Notice
- Warning
- Fatal error

## Próximo item

[Introdução à CLI](https://github.com/PHPSC-Training/php-intro/tree/2-cli-intro)
