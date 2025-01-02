.. _php-usebrowscap:

.. _use-browscap:

Use Browscap
++++++++++++

.. meta::
	:description:
		Use Browscap: Browscap is a browser database, accessible via get_browser().
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Use Browscap
	:twitter:description: Use Browscap: Browscap is a browser database, accessible via get_browser()
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Use Browscap
	:og:type: article
	:og:description: Browscap is a browser database, accessible via get_browser()
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Use Browscap.html
	:og:locale: en
Browscap is a browser database, accessible via `get_browser() <https://www.php.net/get_browser>`_. 

Browscap is the 'Browser Capabilities Project'.

.. code-block:: php
   
   <?php
   echo $_SERVER['HTTP_USER_AGENT'] . "\n\n";
   
   $browser = get_browser(null, true);
   print_r($browser);
   ?>

See also `browscap <http://browscap.org/>`_.

Connex PHP features
-------------------

  + `browscap <https://php-dictionary.readthedocs.io/en/latest/dictionary/browscap.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/UseBrowscap                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.4                                                                                                                                                                                  |
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


