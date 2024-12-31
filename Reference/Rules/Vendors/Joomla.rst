.. _vendors-joomla:

.. _joomla-usage:

Joomla usage
++++++++++++

.. meta\:\:
	:description:
		Joomla usage: This analysis reports usage of the Joomla CMS.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Joomla usage
	:twitter:description: Joomla usage: This analysis reports usage of the Joomla CMS
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Joomla usage
	:og:type: article
	:og:description: This analysis reports usage of the Joomla CMS
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Vendors/Joomla.html
	:og:locale: en
  This analysis reports usage of the Joomla CMS.

.. code-block:: php
   
   <?php
   
   // no direct access
   defined('_JEXEC') or die('Restricted access');
   
   jimport('joomla.application.component.controller');
   JLoader::import('KBIntegrator', JPATH_PLUGINS . DS . 'kbi');
   
   class MyController extends JController {
   	function display($message) {
           echo $message;
       }
   }
   
   ?>

See also `Joomla <http://www.joomla.org/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Joomla                                                                                                                                                                          |
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


