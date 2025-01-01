.. _extensions-extcom:

.. _ext-com:

ext/com
+++++++

.. meta::
	:description:
		ext/com: Extension COM and ``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/com
	:twitter:description: ext/com: Extension COM and ``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/com
	:og:type: article
	:og:description: Extension COM and ``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extcom.html
	:og:locale: en
Extension COM and ``.Net`` (Windows).

COM is an acronym for 'Component Object Model'; it is an object orientated layer (and associated services) on top of DCE RPC (an open standard) and defines a common calling convention that enables code written in any language to call and interoperate with code written in any other language (provided those languages are COM aware).

.. code-block:: php
   
   <?php 
   $domainObject = new COM("WinNT://Domain"); 
   foreach ($domainObject as $obj) { 
      echo $obj->Name . "<br />"; 
   } 
   ?>

See also `COM and .Net (Windows) <https://www.php.net/manual/en/book.com.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extcom                                                                                                                                                                       |
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
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


