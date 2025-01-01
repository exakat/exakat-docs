.. _extensions-extpcre:

.. _ext-pcre:

ext/pcre
++++++++

.. meta::
	:description:
		ext/pcre: Extension ext/pcre.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/pcre
	:twitter:description: ext/pcre: Extension ext/pcre
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/pcre
	:og:type: article
	:og:description: Extension ext/pcre
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extpcre.html
	:og:locale: en
Extension ext/pcre. PCRE stands for Perl Compatible Regular Expression. It is a standard PHP extension.

.. code-block:: php
   
   <?php
   
   $zip_code = $_GET['zip'];
   
   // Canadian Zip code H2M 3J1
   $zip_ca = '/^([a-zA-Z]\d[a-zA-Z])\ {0,1}(\d[a-zA-Z]\d)$/';
   
   // French Zip code  75017
   $zip_fr = '/^\d{5}$/';
   
   // Chinese Zip code  590615
   $zip_cn = '/^\d{6}$/';
   
   var_dump(preg_match($_GET['zip']));
   
   ?>

See also `Regular Expressions (Perl-Compatible) <https://www.php.net/manual/en/book.pcre.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extpcre                                                                                                                                                                      |
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


