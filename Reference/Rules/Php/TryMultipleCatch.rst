.. _php-trymultiplecatch:

.. _try-with-multiple-catch:

Try With Multiple Catch
+++++++++++++++++++++++

.. meta\:\:
	:description:
		Try With Multiple Catch: Try may be used with multiple catch clauses.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Try With Multiple Catch
	:twitter:description: Try With Multiple Catch: Try may be used with multiple catch clauses
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Try With Multiple Catch
	:og:type: article
	:og:description: Try may be used with multiple catch clauses
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Php/TryMultipleCatch.html
	:og:locale: en
  Try may be used with multiple catch clauses.

.. code-block:: php
   
   <?php
   
   try { 
       OneCatch(); 
   } catch (FirstException $e) {
   
   }
   
   try { 
       TwoCatches(); 
   } catch (FirstException $e) {
   } catch (SecondException $e) {
   }
   
   ?>

See also `Exceptions <https://www.php.net/manual/en/language.exceptions.php>`_.

Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/TryMultipleCatch                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.11.3                                                                                                                                                                                  |
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


