.. _vendors-codeigniter:

.. _codeigniter-usage:

Codeigniter usage
+++++++++++++++++

.. meta::
	:description:
		Codeigniter usage: This analysis reports usage of the Codeigniter 4 framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Codeigniter usage
	:twitter:description: Codeigniter usage: This analysis reports usage of the Codeigniter 4 framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Codeigniter usage
	:og:type: article
	:og:description: This analysis reports usage of the Codeigniter 4 framework
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Vendors/Codeigniter.html
	:og:locale: en
This analysis reports usage of the Codeigniter 4 framework.

Note : Code igniter 3 and older are not reported.

.. code-block:: php
   
   <?php
   
   // A code igniter controller
   class Blog extends \App\Controllers\Home {
   
           public function index()
           {
                   echo 'Hello World!';
           }
   }
   
   ?>

See also `Codeigniter <https://codeigniter.com/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Codeigniter                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.8                                                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


