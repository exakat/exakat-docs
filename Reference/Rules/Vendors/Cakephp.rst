.. _vendors-cakephp:

.. _cakephp:

Cakephp
+++++++

.. meta::
	:description:
		Cakephp: This rules reports when the source code is based on the CakePHP framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Cakephp
	:twitter:description: Cakephp: This rules reports when the source code is based on the CakePHP framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Cakephp
	:og:type: article
	:og:description: This rules reports when the source code is based on the CakePHP framework
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Cakephp.html
	:og:locale: en
This rules reports when the source code is based on the CakePHP framework.

CakePHP is an open-source web framework. It follows the model–view–controller (MVC) approach and is written in PHP, modeled after the concepts of Ruby on Rails, and distributed under the MIT License.


.. code-block:: php
   
   <?php
   
   namespace Authentication;
   
   use Cake\Core\ObjectRegistry;
   
   abstract class AbstractCollection extends ObjectRegistry
   {
   }
   
   ?>

See also `CakePHP <https://cakephp.org/>`_.


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Cakephp                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`          |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 2.6.8                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


