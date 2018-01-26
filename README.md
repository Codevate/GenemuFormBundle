# FormBundle
Forked version of the genemu/form-bundle which is compatible with PHP7 and Symfony 3.4.

## Installation

Installation is quick and easy 3 step process:

1. Install GenemuFormBundle
2. Enable the bundle
3. Initialize assets

### Step 1: Install GenemuFormBundle

To use this version of the Genemu Form Bundle, add the following to your `composer.json`:
```
"repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/Codevate/GenemuFormBundle"
        }
],
```

And then require the bundle itself:
```$xslt
"require": {
        "php": ">=7.1",
        "symfony/symfony": "~3.4",
        "genemu/form-bundle": "dev-master",
        ...
},
```
Afterwards you should be able to run `composer update` to download this version of the bundle.
### Step 2: Enable the bundle

Finally, enable the bundle in the kernel:

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    $bundles = array(
        // ...
        new Genemu\Bundle\FormBundle\GenemuFormBundle(),
    );
}
```

### Step 3: Initialize assets

``` bash
$ php bin/console assets:install web/
```

## Form types

### Select2 ([view demo](http://ivaynberg.github.com/select2/)):

[View configuration](https://github.com/genemu/GenemuFormBundle/blob/master/Resources/doc/jquery/select2/index.md)

### Captcha GD

[View configuration](https://github.com/genemu/GenemuFormBundle/blob/master/Resources/doc/captcha_gd/index.md)

### ReCaptcha ([Google library](http://www.google.com/recaptcha)):

[View configuration](https://github.com/genemu/GenemuFormBundle/blob/master/Resources/doc/recaptcha/index.md)

### JQueryUi ([download](http://jqueryui.com/)):

- [Autocomplete](https://github.com/genemu/GenemuFormBundle/blob/master/Resources/doc/jquery/autocomplete/text.md)

### Plain

A Form type that just renders the field as a p tag.
This is useful for forms where certain field need to be shown but not editable.

The type name is ``genemu_plain``.

## Tips

[Prototype usage within form collections](https://github.com/genemu/GenemuFormBundle/blob/master/Resources/doc/tips/form_prototype.md)

## Template

You use GenemuFormBundle and you seen that it does not work!
Maybe you have forgotten ``form_javascript`` or ``form_stylesheet``.

The principle is to separate the javascript, stylesheet and html. This allows better integration of web pages.

[View a template example form view](https://github.com/genemu/GenemuFormBundle/blob/master/Resources/doc/template.md)