.. _structures-shouldchainexception:

.. _should-chain-exception:

Should Chain Exception
++++++++++++++++++++++

.. meta\:\:
	:description:
		Should Chain Exception: Chain exception to provide more context.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Should Chain Exception
	:twitter:description: Should Chain Exception: Chain exception to provide more context
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Should Chain Exception
	:og:type: article
	:og:description: Chain exception to provide more context
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Structures/ShouldChainException.html
	:og:locale: en
  Chain `exception <https://www.php.net/exception>`_ to provide more context.

When catching an `exception <https://www.php.net/exception>`_ and rethrowing another one, it is recommended to chain the `exception <https://www.php.net/exception>`_ : this means providing the original `exception <https://www.php.net/exception>`_, so that the final recipient has a chance to track the origin of the problem. This doesn't change the thrown message, but provides more information.

Note : Chaining requires PHP > 5.3.0.

.. code-block:: php
   
   <?php
       try {
           throw new Exception('Exception 1', 1);
       } catch (\Exception $e) {
           throw new Exception('Exception 2', 2, $e); 
           // Chaining here. 
   
       }
   ?>

See also `Exception::__construct <https://www.php.net/manual/en/exception.construct.php>`_ and `What are the best practices for catching and re-throwing exceptions? <https://stackoverflow.com/questions/5551668/what-are-the-best-practices-for-catching-and-re-throwing-exceptions/5551828>`_.

Connex PHP features
-------------------

  + `exception-chain <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception-chain.ini.html>`_


Suggestions
___________

* Add the incoming exception to the newly thrown exception




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/ShouldChainException                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Examples     | :ref:`case-magento-structures-shouldchainexception`, :ref:`case-tine20-structures-shouldchainexception`                                                                                 |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


