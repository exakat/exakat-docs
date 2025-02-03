.. _php-shellfavorite:


.. _shell-favorite:

Shell Favorite
++++++++++++++

.. meta::
	:description:
		Shell Favorite: PHP has several syntax to make system calls : shell_exec(), exec() and back-ticks, &#96.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Shell Favorite
	:twitter:description: Shell Favorite: PHP has several syntax to make system calls : shell_exec(), exec() and back-ticks, &#96
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Shell Favorite
	:og:type: article
	:og:description: PHP has several syntax to make system calls : shell_exec(), exec() and back-ticks, &#96
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Shell Favorite.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ShellFavorite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/ShellFavorite.html","name":"Shell Favorite","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP has several syntax to make system calls : shell_exec(), exec() and back-ticks, &#96","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Shell Favorite.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP has several syntax to make system calls : `shell_exec() <https://www.php.net/shell_exec>`_, `exec() <https://www.php.net/exec>`_ and back-ticks, &#96; are the common ones. 

It was found that one of those three is actually being used over 90% of the time. The remaining cases should be uniformed, so has to make this code consistent.

.. code-block:: php
   
   <?php
   
   // back-ticks &#96; are only used once.
   &#96;back-tick&#96;;
   
   shell_exec('exec1');
   shell_exec('exec2');
   shell_exec('exec3');
   shell_exec('exec4');
   shell_exec('exec5');
   shell_exec('exec6');
   shell_exec('exec7');
   shell_exec('exec8');
   shell_exec('exec9');
   shell_exec('exec10');
   shell_exec('exec11');
   shell_exec('exec12');
   
   ?>

See also `Execution Operators <https://www.php.net/manual/en/language.operators.execution.php>`_, `shell_exec() <https://www.php.net/shell_exec>`_ and `ptlis/shell-command <https://packagist.org/packages/ptlis/shell-command>`_.

Connex PHP features
-------------------

  + `shell <https://php-dictionary.readthedocs.io/en/latest/dictionary/shell.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ShellFavorite                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.9                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


