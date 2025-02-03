.. _constants-constdefinepreference:


.. _const-or-define-preference:

Const Or Define Preference
++++++++++++++++++++++++++


.. meta::

	:description:

		Const Or Define Preference: ``Const`` and define() have almost the same functional use : they create constants.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: Const Or Define Preference

	:twitter:description: Const Or Define Preference: ``Const`` and define() have almost the same functional use : they create constants

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: Const Or Define Preference

	:og:type: article

	:og:description: ``Const`` and define() have almost the same functional use : they create constants

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Const Or Define Preference.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/ConstDefinePreference.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Constants\/ConstDefinePreference.html","name":"Const Or Define Preference","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"``Const`` and define() have almost the same functional use : they create constants","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Const Or Define Preference.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

``Const`` and `define() <https://www.php.net/define>`_ have almost the same functional use : they create constants. 

The analyzed code has less than 10% of one of them : for consistency reasons, it is recommended to make constant definition consistent. 

It is recommended to use ``const`` for global constants, as this keyword is processed at compile time, while `define() <https://www.php.net/define>`_ is executed.

Note that `define() <https://www.php.net/define>`_ used to allow the creation of case-insensitive constants, but this is deprecated since PHP 7.3 and will be removed in PHP 8.0.

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
       
       const B = 3;
       
   ?>

See also `Constant definition <https://www.php.net/const>`_ and `Define <https://www.php.net/define>`_.

Connex PHP features
-------------------

  + `define <https://php-dictionary.readthedocs.io/en/latest/dictionary/define.ini.html>`_
  + `const <https://php-dictionary.readthedocs.io/en/latest/dictionary/const.ini.html>`_
  + `constant <https://php-dictionary.readthedocs.io/en/latest/dictionary/constant.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Constants/ConstDefinePreference                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.9                                                                                                                   |
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


