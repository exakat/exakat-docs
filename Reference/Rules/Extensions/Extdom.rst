.. _extensions-extdom:

.. _ext-dom:

ext/dom
+++++++

.. meta::
	:description:
		ext/dom: Extension Document Object Model.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/dom
	:twitter:description: ext/dom: Extension Document Object Model
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/dom
	:og:type: article
	:og:description: Extension Document Object Model
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extdom.html
	:og:locale: en
Extension Document Object Model.

The DOM extension allows the manipulation of XML documents through the DOM API with PHP.

.. code-block:: php
   
   <?php
   
   $dom = new DOMDocument('1.0', 'utf-8');
   
   $element = $dom->createElement('test', 'This is the root element!');
   
   // We insert the new element as root (child of the document)
   $dom->appendChild($element);
   
   echo $dom->saveXML();
   ?>

See also `Document Object Model <https://www.php.net/manual/en/book.dom.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extdom                                                                                                                                                                       |
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


