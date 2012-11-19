# SPasswordValidator 1.1

SPasswordValidator is a password validator for the [Yii framework](http://www.yiiframework.com).

It's to use for a form/model validation rule.

## Features

- Ready to use out of the box (see example basic below)

- Presets to choose required strength (_relax_, _normal_, _strong_) 
- Customize parameters 
  - minimum number of characters
  - minimum number of upper case characters
  - minimum number of lower case characters
  - minimum number of digits characters
  - minimum number of special characters
- Documentation included
- Coded using unit tests

## Examples

### Basic (default params)

```php
    public function rules()
    {
        return array(
            array('password','ext.SPasswordValidator.SPasswordValidator')
        );
    }
```

### With preset

```php
    public function rules()
    {
        return array(
            array('password','ext.SPasswordValidator.SPasswordValidator', 'preset' => 'relax');
        );
    }
```

### With custom parameters

Number of upper case chars set to 1, minimum number of characters set to 10.

```php
    public function rules()
    {
        return array(
            array('password','ext.SPasswordValidator.SPasswordValidator', 'up' => 1, 'min' => 10)
        );
    }
```

## Installation 

Uncompress the archive in `protected/extensions/`. So path to php file will be `protected/extensions/SPasswordValidator/SPasswordValidator.php`.

## Problem ?

[Open an issue](https://github.com/SebSept/YiiPasswordValidator/issues).

## Contribute

Use to the [_fullapp_ branch](https://github.com/SebSept/YiiPasswordValidator/tree/fullapp) to fork (include phpunit's unit tests)

## Todo

- Add a 'max' parameter to avoid using another rule for attribute length.

## Licences

This code is published under the [Creative Commons Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0) licence](http://creativecommons.org/licenses/by-sa/3.0/deed).

### Included

The [_fullapp_](https://github.com/SebSept/YiiPasswordValidator/tree/fullapp) branch includes [YiiDocumentor](http://github.com/laMarciana/yiiDocumentor) published under the GNU LESSER GENERAL PUBLIC LICENSE 3
