.. _vendors-concrete5:

.. _concrete5-usage:

Concrete5 usage
+++++++++++++++

.. meta\:\:
	:description:
		Concrete5 usage: This analysis reports usage of the Concrete 5 framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Concrete5 usage
	:twitter:description: Concrete5 usage: This analysis reports usage of the Concrete 5 framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Concrete5 usage
	:og:type: article
	:og:description: This analysis reports usage of the Concrete 5 framework
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Vendors/Concrete5.html
	:og:locale: en
  This analysis reports usage of the Concrete 5 framework.

.. code-block:: php
   
   <?php
   namespace Application\Controller\PageType;
   
   use Concrete\Core\Page\Controller\PageTypeController;
   
   class BlogEntry extends PageTypeController
   {
   
       public function view()
       {
       }
   }
   ?>

See also `Concrete 5 <https://www.concrete5.org/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Concrete5                                                                                                                                                                       |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.9                                                                                                                                                                                   |
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


