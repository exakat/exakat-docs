.. _arrays-withcallback:

.. _handle-arrays-with-callback:

Handle Arrays With Callback
+++++++++++++++++++++++++++

.. meta::
	:description:
		Handle Arrays With Callback: This rule marks method and function calls that accepts array callbacks as argument.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Handle Arrays With Callback
	:twitter:description: Handle Arrays With Callback: This rule marks method and function calls that accepts array callbacks as argument
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Handle Arrays With Callback
	:og:type: article
	:og:description: This rule marks method and function calls that accepts array callbacks as argument
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Handle Arrays With Callback.html
	:og:locale: en
This rule marks method and function calls that accepts array callbacks as argument. 

It marks the method call, and not the argument.

.. code-block:: php
   
   <?php
   
   // Handles arrays with callback
   $uppercase = array_map('strtoupper', $source);
   
   // Handles arrays with foreach
   foreach($source as &$s) {
       $s = uppercase($s);
   }
   
   ?>

See also `array_map <https://www.php.net/array_map>`_.

Connex PHP features
-------------------

  + `callback <https://php-dictionary.readthedocs.io/en/latest/dictionary/callback.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Arrays/WithCallback                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.3.7                                                                                                                                                                                   |
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


