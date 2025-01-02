.. _php-rawpostdatausage:

.. _$http\_raw\_post\_data-usage:

$HTTP_RAW_POST_DATA Usage
+++++++++++++++++++++++++

.. meta::
	:description:
		$HTTP_RAW_POST_DATA Usage: ``$HTTP_RAW_POST_DATA`` is deprecated, and should be replaced by ``php://input``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: $HTTP_RAW_POST_DATA Usage
	:twitter:description: $HTTP_RAW_POST_DATA Usage: ``$HTTP_RAW_POST_DATA`` is deprecated, and should be replaced by ``php://input``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: $HTTP_RAW_POST_DATA Usage
	:og:type: article
	:og:description: ``$HTTP_RAW_POST_DATA`` is deprecated, and should be replaced by ``php://input``
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/$HTTP_RAW_POST_DATA Usage.html
	:og:locale: en
``$HTTP_RAW_POST_DATA`` is deprecated, and should be replaced by ``php://input``. 

``$HTTP_RAW_POST_DATA`` is deprecated since PHP 5.6.

It is possible to prepare code to this lack of feature by setting ``always_populate_raw_post_data`` to -1.

.. code-block:: php
   
   <?php
   
   // PHP 5.5 and older
   $postdata = $HTTP_RAW_POST_DATA;
   
   // PHP 5.6 and more recent
   $postdata = file_get_contents(php://input);
   
   ?>

See also `$HTTP_RAW_POST_DATA variable <https://www.php.net/manual/en/reserved.variables.httprawpostdata.php>`_.

Connex PHP features
-------------------

  + `$HTTP_RAW_POST_DATA <https://php-dictionary.readthedocs.io/en/latest/dictionary/%24HTTP_RAW_POST_DATA.ini.html>`_


Suggestions
___________

* Use php://input with fopen() instead.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/RawPostDataUsage                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP56 <ruleset-CompatibilityPHP56>`                                              |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


