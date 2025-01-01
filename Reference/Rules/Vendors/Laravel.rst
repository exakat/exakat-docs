.. _vendors-laravel:

.. _laravel-usage:

Laravel usage
+++++++++++++

.. meta::
	:description:
		Laravel usage: This analysis reports usage of the Laravel framework.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Laravel usage
	:twitter:description: Laravel usage: This analysis reports usage of the Laravel framework
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Laravel usage
	:og:type: article
	:og:description: This analysis reports usage of the Laravel framework
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Vendors/Laravel.html
	:og:locale: en
This analysis reports usage of the Laravel framework.

.. code-block:: php
   
   <?php
   
   namespace App\Http\Controllers;
   
   use App\User;
   use App\Http\Controllers\Controller;
   
   class UserController extends Controller
   {
       /**
        * Show the profile for the given user.
        *
        * @param  int  $id
        * @return Response
        */
       public function show($id)
       {
           return view('user.profile', ['user' => User::findOrFail($id)]);
       }
   }
   
   ?>

See also `Laravel <http://www.lavarel.com/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Laravel                                                                                                                                                                         |
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


