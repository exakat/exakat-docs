.. _constants-defineinsensitivepreference:

.. _constant-case-preference:

Constant Case Preference
++++++++++++++++++++++++

.. meta::
	:description:
		Constant Case Preference: Define() creates constants which are case sensitive or not.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Constant Case Preference
	:twitter:description: Constant Case Preference: Define() creates constants which are case sensitive or not
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Constant Case Preference
	:og:type: article
	:og:description: Define() creates constants which are case sensitive or not
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Constant Case Preference.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/DefineInsensitivePreference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/DefineInsensitivePreference.html","name":"Constant Case Preference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Sun, 02 Feb 2025 10:12:50 +0000","dateModified":"Sun, 02 Feb 2025 10:12:50 +0000","description":"Define() creates constants which are case sensitive or not","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Constant Case Preference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>`Define() <https://www.php.net/define>`_ creates constants which are case sensitive or not. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make constant sensitivity definition consistent. 

Note that `define() <https://www.php.net/define>`_ used to allow the creation of case-sensitive constants, but this is deprecated since PHP 7.3 and will be removed in PHP 8.0.

.. code-block:: php
   
   <?php
   
       define('A1', 1);
       define('A2', 1);
       define('A3', 1);
       define('A4', 1);
       define('A5', 1);
       define('A6', 1);
       define('A7', 1);
       define('A8', 1);
       define('A9', 1);
       define('A10',1);
       
       define('A10',1, true);
       
   ?>

See also `PHP Constants <https://www.php.net/manual/en/language.constants.php>`_ and `Constant definition <https://www.php.net/const>`_.

Related PHP errors 
-------------------

  + `define(): Declaration of case-insensitive constants is deprecated <https://php-errors.readthedocs.io/en/latest/messages/define%28%29%3A-argument-%233-%28%24case_insensitive%29-is-ignored-since-declaration-of-case-insensitive-constants-is-no-longer-supported.html>`_
  + `define(): Argument #3 ($case_insensitive) is ignored since declaration of case-insensitive constants is no longer supported <https://php-errors.readthedocs.io/en/latest/messages/define%28%29%3A-argument-%233-%28%24case_insensitive%29-is-ignored-since-declaration-of-case-insensitive-constants-is-no-longer-supported.html>`_



Connex PHP features
-------------------

  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/DefineInsensitivePreference                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and older                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


