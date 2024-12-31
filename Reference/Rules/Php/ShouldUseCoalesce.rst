.. _php-shouldusecoalesce:

.. _should-use-coalesce:

Should Use Coalesce
+++++++++++++++++++

.. meta\:\:
	:description:
		Should Use Coalesce: PHP 7 introduced the ``.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Use Coalesce
	:twitter:description: Should Use Coalesce: PHP 7 introduced the ``
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Use Coalesce
	:og:type: article
	:og:description: PHP 7 introduced the ``
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/ShouldUseCoalesce.html
	:og:locale: en
  PHP 7 introduced the ``??`` operator, that replaces longer structures to set default values when a variable is not set.
Sample extracted from PHP docs `Isset Ternary <https://wiki.php.net/rfc/isset_ternary>`_.

.. code-block:: php
   
   <?php
   
   // Fetches the request parameter user and results in 'nobody' if it doesn't exist
   $username = $_GET['user'] ?? 'nobody';
   // equivalent to: $username = isset($_GET['user']) ? $_GET['user'] : 'nobody';
    
   // Calls a hypothetical model-getting function, and uses the provided default if it fails
   $model = Model::get($id) ?? $default_model;
   // equivalent to: if (($model = Model::get($id)) === NULL) { $model = $default_model; }
   
   ?>

See also `New in PHP 7: null coalesce operator <https://lornajane.net/posts/2015/new-in-php-7-null-coalesce-operator>`_.

Connex PHP features
-------------------

  + `coalesce <https://php-dictionary.readthedocs.io/en/latest/dictionary/coalesce.ini.html>`_


Suggestions
___________

* Replace the long syntax with the short one




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/ShouldUseCoalesce                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | With PHP 7.0 and more recent                                                                                                                                                                                           |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-churchcrm-php-shouldusecoalesce`, :ref:`case-cleverstyle-php-shouldusecoalesce`                                                                                                                             |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


