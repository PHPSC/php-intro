# Introdução à CLI - Oficina de introdução à linguagem PHP

Nesta parte vamos falar um pouco sobre a criação de scripts básicos utilizando a linha de comando.
Para isso você deve criar um arquivo qualquer e executá-lo usando o comando ```php```.

Por exemplo:

```sh
echo "<?php echo 'Hello world', PHP_EOL;" > test.php
php test.php
```

## Constantes

```php
<?php
define('TESTING', 1);
const TESTING_2 = 2;
```

## Streams

Usamos fopen, fgets, fwrite, fread, fclose pra trabalhar com streams.

Os streams mais básicos são ```php://stdin```, ```php://stdout``` e ```php://stderr```:

```php
<?php
// Imprime "Testing\n" no buffer de saída
$stdout = fopen('php://stdout', 'w');
fwrite($stdout, "Testing\n");
fclose($stdout);

// Imprime "Testing\n" no buffer de erro
$stderr = fopen('php://stderr', 'w');
fwrite($stderr, "Testing\n");
fclose($stderr);

// Lê do buffer de entrada (até a quebra de linha)
$stdin = fopen('php://stdin', 'r');
echo fgets($stdin);
fclose($stdin);
```

O PHP disponibiliza as constantes ```STDIN```, ```STDOUT``` e ```STDERR``` para facilitar nosso trabalho:

```php
<?php
// Imprime "Testing\n" no buffer de saída
fwrite(STDOUT, "Testing\n");

// Imprime "Testing\n" no buffer de erro
fwrite(STDERR, "Testing\n");

// Lê do buffer de entrada (até a quebra de linha)
echo fgets(STDIN);
```

O comando ```echo``` escreve por padrão no STDOUT.

## Códigos de saída

Todo comando tem um código de saída que deve estar entre 0-255.
O 0 significa que o programa executou com sucesso, códigos maiores que 0 significam erros.

Através da função ```exit()``` podemos alterar o código de saída de um script:

```php
<?php
echo "Digite seu nome: ";
$name = trim(fgets(STDIN));

if (strlen($name) > 10) {
    fwrite(STDERR, "Nome muito longo");
    exit(1);
}

echo "Bem vindo $name\n";
```

## Próximo item

[Funções](https://github.com/PHPSC-Training/php-intro/tree/3-functions)
