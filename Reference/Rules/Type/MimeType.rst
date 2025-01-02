.. _type-mimetype:

.. _mime-types:

Mime Types
++++++++++

.. meta::
	:description:
		Mime Types: List of Mime Types that are mentioned in the code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Mime Types
	:twitter:description: Mime Types: List of Mime Types that are mentioned in the code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Mime Types
	:og:type: article
	:og:description: List of Mime Types that are mentioned in the code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Mime Types.html
	:og:locale: en
List of Mime Types that are mentioned in the code.

.. code-block:: php
   
   <?php
   
   $mimeType = 'multipart/form-data';
   $mimeType = 'image/jpeg';
   $mimeType = 'application/zip';
   
   header('Content-Type: '.$mimeType);
   
   ?>

See also `Media Type <https://en.wikipedia.org/wiki/Media_type>`_ and `MIME <https://en.wikipedia.org/wiki/MIME>`_..


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Type/MimeType                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Inventory <ruleset-Inventory>`      |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


