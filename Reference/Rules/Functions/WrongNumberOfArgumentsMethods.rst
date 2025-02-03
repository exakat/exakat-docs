.. _functions-wrongnumberofargumentsmethods:

.. _wrong-number-of-arguments-in-methods:

Wrong Number Of Arguments In Methods
++++++++++++++++++++++++++++++++++++

.. meta::
	:description:
		Wrong Number Of Arguments In Methods: Those methods are called with a wrong number of arguments : too many or too few.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Wrong Number Of Arguments In Methods
	:twitter:description: Wrong Number Of Arguments In Methods: Those methods are called with a wrong number of arguments : too many or too few
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Wrong Number Of Arguments In Methods
	:og:type: article
	:og:description: Those methods are called with a wrong number of arguments : too many or too few
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Wrong Number Of Arguments In Methods.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongNumberOfArgumentsMethods.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Functions\/WrongNumberOfArgumentsMethods.html","name":"Wrong Number Of Arguments In Methods","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:47:06 +0000","dateModified":"Fri, 10 Jan 2025 09:47:06 +0000","description":"Those methods are called with a wrong number of arguments : too many or too few","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Wrong Number Of Arguments In Methods.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Those methods are called with a wrong number of arguments : too many or too few. Check the signature.
Methods with a variable number of argument, either using ellipsis or `func_get_args() <https://www.php.net/func_get_args>`_ are ignored. 

PHP emits an `error <https://www.php.net/error>`_ at runtime, when arguments are not enough : ''. PHP doesn't emit an `error <https://www.php.net/error>`_ when too many arguments are provided.

.. code-block:: php
   
   <?php
   
   class Foo {
       private function Bar($a, $b) {
           return $a + $b;
       }
       
       public function foobar() {
           $this->Bar(1);
           
           // Good amount
           $this->Bar(1, 2);
           
           // Too Many
           $this->Bar(1, 2, 3);
       }
   }
   
   ?>
Related PHP errors 
-------------------

  + `Too few arguments to function Foo::Bar(), 1 passed <https://php-errors.readthedocs.io/en/latest/messages/too-few-arguments-to-function-%25s%25s%25s%28%29%2C-%25d-passed-and-%25s-%25d.html>`_



Connex PHP features
-------------------

  + `composer <https://php-dictionary.readthedocs.io/en/latest/dictionary/composer.ini.html>`_


Suggestions
___________

* Adapt the call to use one of the right number of arguments : this means dropping the extra ones, or adding the missing ones
* Adapt the signature of the method, and use a default value




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/WrongNumberOfArgumentsMethods                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
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


