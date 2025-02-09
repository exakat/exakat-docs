.. _functions-isextfunction:


.. _is-an-extension-function:

Is An Extension Function
++++++++++++++++++++++++

.. meta::
	:description:
		Is An Extension Function: This is an extension function.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Is An Extension Function
	:twitter:description: Is An Extension Function: This is an extension function
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Is An Extension Function
	:og:type: article
	:og:description: This is an extension function
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Is An Extension Function.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/IsExtFunction.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/IsExtFunction.html","name":"Is An Extension Function","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"This is an extension function","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Is An Extension Function.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

This is an extension function. 
Almost every PHP extension defines extra functions. Nowadays, they are prefixed, like ``mysqli_connect``, ``ldap_close``, or ``zlib_decode``. Sometimes, they are even in a namespace. Refer to the extension itself to learn more about its functions usage.

.. code-block:: php
   
   <?php
   
   // range is a native PHP function. It is always available
   $array = range(0, 100);
   
   // json_encode is an extension function : it requires that PHP was compile with ext/json
   echo json_encode($array);
   
   ?>
Connex PHP features
-------------------

  + `Functions <https://php-dictionary.readthedocs.io/en/latest/dictionary/function.ini.html>`_
  + `Extensions <https://php-dictionary.readthedocs.io/en/latest/dictionary/extension.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/IsExtFunction                                                                                                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Deprecated <ruleset-Deprecated>`                                            |
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


