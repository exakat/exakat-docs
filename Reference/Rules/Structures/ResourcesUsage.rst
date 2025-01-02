.. _structures-resourcesusage:

.. _resources-usage:

Resources Usage
+++++++++++++++

.. meta::
	:description:
		Resources Usage: List of situations that are creating resources.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Resources Usage
	:twitter:description: Resources Usage: List of situations that are creating resources
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Resources Usage
	:og:type: article
	:og:description: List of situations that are creating resources
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Resources Usage.html
	:og:locale: en
List of situations that are creating resources.

.. code-block:: php
   
   <?php
       // This functioncall creates a resource to use
       $fp = fopen('/tmp/file.txt', 'r');
       
       if (!is_resource($fp)){
           thrown new RuntimeException('Could not open file.txt');
       }
   ?>
Connex PHP features
-------------------

  + `resource <https://php-dictionary.readthedocs.io/en/latest/dictionary/resource.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ResourcesUsage                                                                                                                                                               |
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


