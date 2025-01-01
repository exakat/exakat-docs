.. _functions-unbindingclosures:

.. _unbinding-closures:

Unbinding Closures
++++++++++++++++++

.. meta::
	:description:
		Unbinding Closures: Never drop ``$this``, once a closure was created in a non-static method.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Unbinding Closures
	:twitter:description: Unbinding Closures: Never drop ``$this``, once a closure was created in a non-static method
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Unbinding Closures
	:og:type: article
	:og:description: Never drop ``$this``, once a closure was created in a non-static method
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Functions/UnbindingClosures.html
	:og:locale: en
Never drop ``$this``, once a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ was created in a non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ method. 

From the PHP wiki : "Currently it is possible to unbind the `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ variable from a `closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_ that originally had one by using ``$`closure <https://www.php.net/`closure <https://www.php.net/closure>`_>`_->bindTo(null)``. Due to the removal of `static <https://www.php.net/manual/en/language.oop5.static.php>`_ calls to non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods in PHP 8, we now have a guarantee that `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ always exists inside non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods. We would like to have a similar guarantee that `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ always exists for non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ closures declared inside non-`static <https://www.php.net/manual/en/language.oop5.static.php>`_ methods. Otherwise, we will end up imposing an unnecessary performance penalty either on `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ accesses in general, or `$this <https://www.php.net/manual/en/language.oop5.basic.php>`_ accesses inside such closures." 

Calling ``bindTo()`` with a valid object is still valid.



.. code-block:: php
   
   <?php
   
   class x {
       private $a = 3;
       
       function foo() {
           return function () { echo $this->a; };
       }
   }
   
   $closure = (new x)->foo();
   
   // $this was expected, and it is not anymore
   $closure->bindTo(null);
   
   $closure->bindTo(new x);
   
   ?>

See also `Unbinding $this from non-static closures <https://wiki.php.net/rfc/deprecations_php_7_4#unbinding_this_from_non-static_closures>`_.

Connex PHP features
-------------------

  + `closure <https://php-dictionary.readthedocs.io/en/latest/dictionary/closure.ini.html>`_
  + `closure-binding <https://php-dictionary.readthedocs.io/en/latest/dictionary/closure-binding.ini.html>`_


Suggestions
___________

* Create a static closure, which doesn't rely on $this at all
* Remove the call to ``bindTo(null)``.




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Functions/UnbindingClosures                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`CE <ruleset-CE>`, :ref:`CompatibilityPHP74 <ruleset-CompatibilityPHP74>`                                                                                |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 1.9.0                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Minor                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Quick (30 mins)                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


