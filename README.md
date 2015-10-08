# Funções - Oficina de introdução à linguagem PHP

Para organizar melhor nossos scritps podemos criar funções e procedimentos. O PHP disponibiliza
a estrutura ```function``` para isso:

```php
<?php
function test($one, $other) {
    return $one . " " . $other . PHP_EOL;
}

echo test("Hello", "World");
echo test("Hello", "Luís");

// Parametros com valor padrão
function test2($one = 'Hello', $other = 'World') {
    return $one . " " . $other . PHP_EOL;
}

echo test2();
echo test2("Hi");

// Funções anônimas
$testing = function () {
    echo "Hello there!\n";
};

$testing();
```

## Próximo item

[Arquivos](https://github.com/PHPSC-Training/php-intro/tree/4-files)
