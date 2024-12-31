.. _vendors-wordpress:

.. _wordpress-usage:

Wordpress usage
+++++++++++++++

.. meta\:\:
	:description:
		Wordpress usage: This analysis reports usage of the Wordpress platform.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wordpress usage
	:twitter:description: Wordpress usage: This analysis reports usage of the Wordpress platform
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wordpress usage
	:og:type: article
	:og:description: This analysis reports usage of the Wordpress platform
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Vendors/Wordpress.html
	:og:locale: en
  This analysis reports usage of the Wordpress platform.

The current supported version is Wordpress 5.8.

.. code-block:: php
   
   <?php
   
   //Usage of the WP_http class from Wordpress
   $rags = array(
      'x' => '1',
      'y' => '2'
   );
   $url = 'http://www.example.com/';
   $request = new WP_Http();
   $result = $request->request( $url, array( 'method' => 'POST', 'body' => $body) );
   
   ?>

See also `Wordpress <https://www.wordpress.org/>`_.

Connex PHP features
-------------------

  + `framework <https://php-dictionary.readthedocs.io/en/latest/dictionary/framework.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Vendors/Wordpress                                                                                                                                                                       |
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


