## Timber 2.0 For ClassicPress 2

## What is Timber For ClassicPress?

Timber helps you create fully-customized WordPress themes faster with more sustainable code. With Timber, you write your HTML using the [Twig Template Engine](https://twig.symfony.com/) separate from your PHP files.

This cleans up your theme code so, for example, your PHP file can focus on being the data/logic, while your Twig file can focus 100% on the HTML and display.

This is what Timber's `.twig` files look like (from this [Hello World example](https://gist.github.com/jarednova/dc75030fd2c7dd6fe52a6fef459c450e))

***This version of Timber has been made to be compatible with ClassicPress 2***.

```twig
{% extends "base.twig" %}

{% block content %}
  <h1 class="big-title">{{ foo }}</h1>
  <h2 class="post-title">{{ post.title }}</h2>

  <img src="{{ post.thumbnail.src }}" />

  <div class="body">
	{{ post.content }}
  </div>
{% endblock %}
```

Once Timber is installed, it gives any WordPress theme the ability to take advantage of the power of Twig and other Timber features.

## Documentation

* [Timber Documentation](https://timber.github.io/docs/)
* [Twig Reference](https://twig.symfony.com/doc/3.x/)
* [Overview / Getting Started Guide](https://timber.github.io/docs/v2/getting-started/introduction/)

* * *

### Installation

Use Composer to install.

```
composer require tuxedosoft/timber

```

### Main Difference From The WordPress Version

This version does away with the Blocks check. ClassicPress does not use the Blocks Editor.


### About The StarterSite

The *StarterSite.php* allows Timber's Starter Theme (or your Timber theme) to 'play nice' with ClassicPress. It does away with the ***add_theme_support('html5')*** since starting from ClassicPress 2 *add_theme_support('html5')* is deprecated.

Simply, copy this file and replace the *src/StarterSite.php* in your Timber theme for things to work right.

### Who is it good for?

Timber is great for any WordPress/ClassicPress developer who cares about writing good, maintainable code. It helps teams of designers and developers working together. With Timber your best WordPress/ClassicPress engineer can focus on building the `.php` files with requests from WordPress/ClassicPress and pass the data into `.twig` files. Once there, designers can easily mark-up data and build out a site's look-and-feel.

### Should I use it?

Timber is MIT-licensed, so please use in personal or commercial work. Just don't re-sell it.

## Documentation

The Official [Documentation for Timber](https://timber.github.io/docs/).
