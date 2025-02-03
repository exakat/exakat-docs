.. _exceptions-catche:


.. _caught-variable:

Caught Variable
+++++++++++++++

.. meta::
	:description:
		Caught Variable: Catch clauses require an exception and a variable name.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Caught Variable
	:twitter:description: Caught Variable: Catch clauses require an exception and a variable name
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Caught Variable
	:og:type: article
	:og:description: Catch clauses require an exception and a variable name
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Caught Variable.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/CatchE.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/CatchE.html","name":"Caught Variable","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Catch clauses require an exception and a variable name","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Caught Variable.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Catch clauses require an `exception <https://www.php.net/exception>`_ and a variable name. Often, the variable name is the same, `$e`, as learnt from the manual.

There seems to be a choice that is not enforced : one form is dominant, (> 90%) while the others are rare. 

The analyzed code has less than 10% of one of the three : for consistency reasons, it is recommended to make them all the same.

.. code-block:: php
   
   <?php
   
   try {
       // do Something()
   }
   catch (MyException1 $e)       { $log->log($e->getMessage();}
   catch (MyException2 $e)       { $log->log($e->getMessage();}
   catch (MyException3 $e)       { $log->log($e->getMessage();}
   catch (MyException4 $e)       { $log->log($e->getMessage();}
   catch (MyException5 $e)       { $log->log($e->getMessage();}
   catch (MyException6 $e)       { $log->log($e->getMessage();}
   catch (MyException7 $e)       { $log->log($e->getMessage();}
   catch (MyException8 $e)       { $log->log($e->getMessage();}
   catch (MyException9 $e)       { $log->log($e->getMessage();}
   catch (MyException10 $e)      { $log->log($e->getMessage();}
   catch (\RuntimeException $e)  { $log->log($e->getMessage();}
   catch (\Error $error)         { $log->log($error->getMessage();}
   catch (\Exception $exception) { $log->log($exception->getMessage();}
   ?>
Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Make all caught constant consistent, and avoid using them for something else




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/CatchE                                                                                                       |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Preferences <ruleset-Preferences>`  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.7.6                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


