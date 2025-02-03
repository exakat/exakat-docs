.. _structures-noreturninfinally:


.. _no-return-or-throw-in-finally:

No Return Or Throw In Finally
+++++++++++++++++++++++++++++


.. meta::

	:description:

		No Return Or Throw In Finally: Avoid using return and throw in a finally block.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: No Return Or Throw In Finally

	:twitter:description: No Return Or Throw In Finally: Avoid using return and throw in a finally block

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: No Return Or Throw In Finally

	:og:type: article

	:og:description: Avoid using return and throw in a finally block

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/No Return Or Throw In Finally.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoReturnInFinally.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/NoReturnInFinally.html","name":"No Return Or Throw In Finally","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Avoid using return and throw in a finally block","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/No Return Or Throw In Finally.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Avoid using return and throw in a finally block. Both command will interrupt the processing of the try catch block, and any `exception <https://www.php.net/exception>`_ that was emitted will not be processed. This leads to unprocessed exceptions, leaving the application in an unstable state.

Note that PHP prevents the usage of goto, `break <https://www.php.net/manual/en/control-structures.break.php>`_ and `continue <https://www.php.net/manual/en/control-structures.continue.php>`_ within the finally block at linting phase. This is categorized as a Security problem.

.. code-block:: php
   
   <?php
   function foo() {
           try {
               // Exception is thrown here 
               throw new \Exception();
           } catch (Exception $e) {
               // This is executed AFTER finally
               return 'Exception';
           } finally {
               // This is executed BEFORE catch
               return 'Finally';
           }
       }
   }
   
   // Displays 'Finally'. No exception
   echo foo();
   
   function bar() {
           try {
               // Exception is thrown here 
               throw new \Exception();
           } catch (Exception $e) {
               // Process the exception. 
               return 'Exception';
           } finally {
               // clean the current situation
               // Keep running the current function
           }
           return 'Finally';
       }
   }
   
   // Displays 'Exception', with processed Exception
   echo bar();
   
   ?>

See also `Return Inside Finally Block <https://www.owasp.org/index.php/Return_Inside_Finally_Block>`_.

Connex PHP features
-------------------

  + `finally <https://php-dictionary.readthedocs.io/en/latest/dictionary/finally.ini.html>`_
  + `return <https://php-dictionary.readthedocs.io/en/latest/dictionary/return.ini.html>`_


Suggestions
___________

* Move the return right after the try/catch/finally call




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/NoReturnInFinally                                                                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.1                                                                                                                  |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


