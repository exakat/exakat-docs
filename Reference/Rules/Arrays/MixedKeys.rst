.. _arrays-mixedkeys:

.. _mixed-keys-in-array:

Mixed Keys In Array
+++++++++++++++++++

.. meta::
	:description:
		Mixed Keys In Array: Avoid mixing constants and literals in array keys.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mixed Keys In Array
	:twitter:description: Mixed Keys In Array: Avoid mixing constants and literals in array keys
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mixed Keys In Array
	:og:type: article
	:og:description: Avoid mixing constants and literals in array keys
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Arrays/MixedKeys.html
	:og:locale: en
Avoid mixing constants and literals in array keys.

When defining default values in arrays, it is recommended to avoid mixing constants and literals, as PHP may mistake them and overwrite the previous with the latter.

Either switch to a newer version of PHP (5.5 or newer), or make sure the resulting array hold the expected data. If not, reorder the definitions.

.. code-block:: php
   
   <?php
   
   const ONE = 1;
   
   $a = [ 1   => 2,
          ONE => 3];
   
   ?>
Connex PHP features
-------------------

  + `array <https://php-dictionary.readthedocs.io/en/latest/dictionary/array.ini.html>`_


Suggestions
___________

* Use only literals or constants when building the array




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/MixedKeys                                                                                                                         |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CompatibilityPHP53 <ruleset-CompatibilityPHP53>`, :ref:`CompatibilityPHP54 <ruleset-CompatibilityPHP54>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 5.6 and more recent                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                            |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                     |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------+


