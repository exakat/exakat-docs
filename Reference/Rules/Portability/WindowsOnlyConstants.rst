.. _portability-windowsonlyconstants:

.. _windows-only-constants:

Windows Only Constants
++++++++++++++++++++++

.. meta::
	:description:
		Windows Only Constants: When built on Windows, PHP offers some extra constants.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Windows Only Constants
	:twitter:description: Windows Only Constants: When built on Windows, PHP offers some extra constants
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Windows Only Constants
	:og:type: article
	:og:description: When built on Windows, PHP offers some extra constants
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Portability/WindowsOnlyConstants.html
	:og:locale: en
When built on Windows, PHP offers some extra constants. They are not available on other operating systems.

.. code-block:: php
   
   <?php
   
   //The Windows build number (for example, Windows Vista with SP1 applied is build 6001)
   echo PHP_WINDOWS_VERSION_BUILD;
   
   ?>

See also `Info Predefined Constants <https://www.php.net/manual/en/info.constants.php>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Portability/WindowsOnlyConstants                                                                                        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.0                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


