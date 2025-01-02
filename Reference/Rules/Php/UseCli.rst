.. _php-usecli:

.. _use-cli:

Use Cli
+++++++

.. meta::
	:description:
		Use Cli: Signal the usage of code in CLI mode, through the usage of ``$argv`` and ``$argc`` variables, or the getopt() function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Cli
	:twitter:description: Use Cli: Signal the usage of code in CLI mode, through the usage of ``$argv`` and ``$argc`` variables, or the getopt() function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Cli
	:og:type: article
	:og:description: Signal the usage of code in CLI mode, through the usage of ``$argv`` and ``$argc`` variables, or the getopt() function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Cli.html
	:og:locale: en
Signal the usage of code in CLI mode, through the usage of ``$argv`` and ``$argc`` variables, or the `getopt() <https://www.php.net/getopt>`_ function.

.. code-block:: php
   
   <?php
   
   // Characteristics of CLI usage 
   getopt("abcd");
   
   ?>
Connex PHP features
-------------------

  + `cli <https://php-dictionary.readthedocs.io/en/latest/dictionary/cli.ini.html>`_
  + `$argv <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24argv.ini.html>`_
  + `$argc <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24argc.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseCli                                                                                                                                                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


