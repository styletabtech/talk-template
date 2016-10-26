[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Intro to PHP


## Preparation

1.  Fork this repository if you'd like.


## What is PHP?

PHP is a widely-used open source general-purpose scripting language that is especially suited for server-side web development and can be embedded into HTML.

It was created in 1994 by
Rasmus Lerdorf. It’s original use was for tracking visits to his online resume and at the time PHP stood for Personal Homepage. Today, PHP stands for PHP: Hypertext Preprocessor and does way more than tracking visits on Rasmus's personal home page.

PHP can do a variety of things:
- evaluate form data sent from a browser
- build custom web content to serve the browser
- talk to a database
- send and receive cookies

```
<!DOCTYPE HTML>
<html>
    <head>
        <title>Example</title>
    </head>
    <body>

        <?php
            echo "Hi, I'm a PHP script!";
        ?>

    </body>
</html>
```
- PHP-enabled web pages are treated just like regular HTML pages and you can create and edit them the same way you normally create regular HTML pages.

- What distinguishes PHP from something like client-side JavaScript is that the code is executed on the server, generating HTML which is then sent to the client. The client would receive the results of running that script, but would not know what the underlying code was. You can even configure your web server to process all your HTML files with PHP, and then there's really no way that users can tell what you have up your sleeve.


## Syntax

- PHP code is always starts with a tag`<?php` and end with `?>`
- PHP statements end with a semi-colon.
- Blocks are contained within curly braces.
- `echo` is used to print stuff, similar to return or puts

## Variables
- `$newVariable` The dollar sign is used to declare a new variable, just like let or const.
- `$newVariable = foo` You assign values to variables using the assignment operator, equal sign.
- PHP variables don’t have to be declared before they are used. Setting a variable for the first time is simultaneously declaring that variable.
- Variable names are typically used in camelCase but you may also see snake_case.

## Concatenation / String Interpolation
- For concatenation, the `.` is used, similar to how the `+` is used in Javascript.
- For string interpolation `“”` and `‘’` will print different things. You'll want to use `""` for string interpolation.
- filename should end in .php

## Data Types

PHP has 8 data types

- Strings
- Integers
- Floating point numbers
- Booleans
- Arrays
- Objects
- Resource
- NULL

- The falsy values of PHP are: FALSE NULL 0 0.0 "0" `''` `[]`

In PHP you don’t have to explicitly set a variable’s data type. For example, PHP is smart enough to guess that you want this to be an integer:
`$myNum = 25;`

PHP is also smart enough to know that if you try to perform operations on different variables with different data types it will still perform the operation. Example:
```
"10" * 2  # this will output to 20
```

- To get the datatype of something you can use 'gettype();' this is bulit into PHP.

- Type casting. If you’d like to explicitly set a variable’s data type, you can do so with type casting. This is done by prefixing a value with your desired type in parens.

```
$apples = (int)10.6339;  # Cast to an Integer
echo gettype($apples) # Outputs "integer"
echo $apples;         # Outputs 10
```

# Flow Control
## Conditionals

If statements are just as you know them in JavaScript.

```
<?php
  $name = "Edgar";

  if ($name == "Simon") {
    print "I know you!";
  }
  else {
    print "Who are you?";
  }
?>
```
##Loops
Same with loops!
```
<?php

for ($i = 1; $i <= 10; $i++) {
    echo $i;
}
```
## Functions

- Function names typically use camel case, and do not need a dollar sign.
- However, their arguements have the same syntax as variables and need a dollar sign.
- Any valid PHP code may appear inside a function, even other functions and class definitions.
- Functions need not be defined before they are referenced, except when a function is conditionally defined
- When a function is defined in a conditional manner its definition must be processed prior to being called.
```
<?php
function foo($arg_1, $arg_2, /* ..., */ $arg_n)
{
    echo "Example function.\n";
    return $retval;
}
?>
```


## Application
- PHP can be used on all major operating systems
- With PHP, you have the freedom of choosing an operating system and a web server. Furthermore, you also have the choice of using procedural programming or object oriented programming (OOP), or a mixture of them both.
- With PHP you are not limited to output HTML. PHP's abilities includes outputting images and PDF files generated on the fly.
- One of the strongest and most significant features in PHP is its support for a wide range of databases.


## Laravel

- One of the most popular frameworks to use with PHP
- It's free and open-source.
- It follows the MVC architectural pattern
- Laravel is to PHP, as Rails is to Ruby
- LAMP stack - Laravel, Apache, MySql, PHP
- [Laravel documentation](https://laravel.com/docs/5.3)

## Additional Resources

- [Codecademy's PHP course](https://www.codecademy.com/learn/php)
-   [PHP documentation](http://www.php.net/manual/en/getting-started.php)
- [Derek Banas's PHP YouTube tutorials](https://www.youtube.com/watch?v=l21g8dJmD7U&list=PL21E20F9A122DC853)
-  [PHP the right way](http://www.phptherightway.com/)
-   [History of PHP](http://php.net/manual/en/history.php.php)
- [Taking PHP seriously](https://slack.engineering/taking-php-seriously-cf7a60065329#.fiqwmmrp8)

## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.
