.. _security-sessioncacheddata:

.. _unvalidated-data-cached-in-session:

Unvalidated Data Cached In Session
++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Unvalidated Data Cached In Session: Data is cached in the $_SESSION variable and later reused.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unvalidated Data Cached In Session
	:twitter:description: Unvalidated Data Cached In Session: Data is cached in the $_SESSION variable and later reused
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unvalidated Data Cached In Session
	:og:type: article
	:og:description: Data is cached in the $_SESSION variable and later reused
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Security/SessionCachedData.html
	:og:locale: en
Data is cached in the $_SESSION variable and later reused. When data is not validated before this storage, it might be used to make an injection.

.. code-block:: php
   
   <?php
   
   $_SESSION['a'] = $_GET['a'];
   
   // across the code, this call
   function foo() {
   	echo $_SESSION["a"];
   }
   
   ?>

Suggestions
___________

* Validate data before storing in the SESSION




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/SessionCachedData                                                                                              |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.5.2                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Medium                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


