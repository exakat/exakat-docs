.. _exceptions-overwriteexception:


.. _overwritten-exceptions:

Overwritten Exceptions
++++++++++++++++++++++

.. meta::
	:description:
		Overwritten Exceptions: In catch blocks, it is good practice to avoid overwriting the incoming exception, as information about the exception will be lost.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Overwritten Exceptions
	:twitter:description: Overwritten Exceptions: In catch blocks, it is good practice to avoid overwriting the incoming exception, as information about the exception will be lost
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Overwritten Exceptions
	:og:type: article
	:og:description: In catch blocks, it is good practice to avoid overwriting the incoming exception, as information about the exception will be lost
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Overwritten Exceptions.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/OverwriteException.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Exceptions\/OverwriteException.html","name":"Overwritten Exceptions","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"In catch blocks, it is good practice to avoid overwriting the incoming exception, as information about the exception will be lost","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Overwritten Exceptions.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

In catch blocks, it is good practice to avoid overwriting the incoming `exception <https://www.php.net/exception>`_, as information about the `exception <https://www.php.net/exception>`_ will be lost.

.. code-block:: php
   
   <?php
   
   try {
       doSomething();
   } catch (SomeException $e) { 
       // $e is overwritten 
       $e = new anotherException($e->getMessage()); 
       throw $e;
   } catch (SomeOtherException $e) { 
       // $e is chained with the next exception 
       $e = new Exception($e->getMessage(), 0, $e); 
       throw $e;
   }
   
   ?>
Connex PHP features
-------------------

  + `exception <https://php-dictionary.readthedocs.io/en/latest/dictionary/exception.ini.html>`_


Suggestions
___________

* Use another variable name to create new values inside the catch
* Use anonymous catch clause (no variable caught) in PHP 8.0, to make this explicit




Specs
_____

+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exceptions/OverwriteException                                                                                                                                                                                          |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Suggestions <ruleset-Suggestions>` |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                                                    |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                                                  |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                                                        |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                                                              |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                                |
+--------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


