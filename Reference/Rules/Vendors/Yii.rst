.. _vendors-yii:

.. _yii-usage:

Yii usage
+++++++++

.. meta::
	:description:
		Yii usage: This analysis reports usage of the Yii 2 framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Yii usage
	:twitter:description: Yii usage: This analysis reports usage of the Yii 2 framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Yii usage
	:og:type: article
	:og:description: This analysis reports usage of the Yii 2 framework
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Vendors/Yii.html
	:og:locale: en
This analysis reports usage of the Yii 2 framework.

This analysis targets Yii 2, not Yii 1.

.. code-block:: php
   
   <?php
   
   // A Yii controller
   class SiteController extends \Yii\Web\Controller
   {
       public function actionIndex()
       {
           // ...
       }
    
       public function actionContact()
       {
           // ...
       }
   }
   
   ?>

See also `Yii <http://www.yiiframework.com/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Yii                                                                                                                                                                             |
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


