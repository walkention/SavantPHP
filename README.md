SavantPHP - The Simple, Elegant Template System For PHP
=======================================================

SavantPHP is a lightweight object-oriented template system for PHP. It aims at ONE thing, being a simple & light-weight TEMPLATING system. I'm focusing only on that ONE thing. PHP can do everything, so do everything with it, just use SavantPHP for only separating the "view/templating" concern, that's it.

Unlike other template systems, Savant by default does not compile your templates into PHP; instead, it uses PHP itself as its template language so you don't need to learn a new markup system.

It is not a competitor to any of the likes of Dwoo or Twig..etc. SavantPHP is for those PHP/templating minimalists - "I just want to separate my front layer(view) from the back layer(code logic)" in the most simple & effective way and that's it, nothing more, nothing less, nothing else (no added crap).

### How To Install

composer require sevenphp/savantphp

### Why Use Savant for Templates?


- You don't need to learn a new language or markup to create a template. The template language is PHP, and the template file is a regular PHP file.
- Because your template script is a regular PHP script, you can sprinkle it with comments and use phpDocumentor to document it.
- No need to assign variable to an array before you can use it inside your template. The variable usage is more direct and simple. (see example code below)

Example:

```php

/* file.php */
$tpl = new Savant(['template_path' => '/path/to/yourViews/']);
$tpl->mynameis = 'Wasseem';

$tpl->setTemplate('file.tpl.php');
$tpl->display(); //or $response = $tpl->getOutput();

```

```php

/* file.tpl.php */
<html>
<head></head>
<body>
    <p>Hello, my name is <?php if(isset($this->mynameis)) echo $this->escape($this->mynameis) ?></p>
<body>
</html>

```

Voila! Simple huh?

### Attention

- While SavantPHP does provide the **$this->escape()** to sanitize your output, it's your responsibility to filter and sanitize your input deeply inside your 'coding back' (php code file). The aim with SavantPHP is only to act as a templating system, the rest is upon you!

### CREDIT

- This project has been retouched by Khayrattee on Dec 2015 to keep the spirit of Savant which was **started & created by The Mighty 'Paul M. Jones' who is the author of [Aura PHP](https://github.com/auraphp).**
- This project was handed over to Brett Bieber, but it seems it has been shamelessly abandoned as well as it's domain name. And he seems not so keen to be positive to PRs and on top of that no single sign of positivity in terms of pushing this project forward - too sad!
- This project is hence a FORK from [https://github.com/saltybeagle/Savant3], but reworked to having namespaces & composer magic & slimming down the aim of Savant - **hence the new name Savant PHP**.

### NOTE

- I have removed the Filter & Plugin System. If you need them, see version tagged v1.0.0

### The Future

- I have been a big fan and user of Savant. I decided to keep it alive and I'm still using it.
- I am not sure how far this will go, but I'm going to leave it here so that it can be used with the latest tools like composer, making it have proper namespace..etc just for me (and perhaps some others) to keep using it.
- Savant PHP still makes very much sense using as it honors the KISS principle. I like to keep it simple.

### Your Contribution

- Please help in testing and improving it.
- Send your pull request on github.
- And report any bugs either via email (savantphp@7php.com) or via github issues.
(thanks guys!)
