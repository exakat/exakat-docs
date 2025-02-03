.. _php-sethandlers:


.. _php-handlers-usage:

PHP Handlers Usage
++++++++++++++++++

.. meta::
	:description:
		PHP Handlers Usage: PHP has a number of handlers that may be replaced by customized code : session, shutdown, error, exception.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: PHP Handlers Usage
	:twitter:description: PHP Handlers Usage: PHP has a number of handlers that may be replaced by customized code : session, shutdown, error, exception
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: PHP Handlers Usage
	:og:type: article
	:og:description: PHP has a number of handlers that may be replaced by customized code : session, shutdown, error, exception
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/PHP Handlers Usage.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/SetHandlers.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Php\/SetHandlers.html","name":"PHP Handlers Usage","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"PHP has a number of handlers that may be replaced by customized code : session, shutdown, error, exception","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/PHP Handlers Usage.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

PHP has a number of handlers that may be replaced by customized code : session, shutdown, `error <https://www.php.net/error>`_, `exception <https://www.php.net/exception>`_. They are noted here.

The example is adapted from the PHP documentation of `set_error_handler() <https://www.php.net/set_error_handler>`_.

.. code-block:: php
   
   <?php
   // error handler function
   function myErrorHandler($errno, $errstr, $errfile, $errline)
   {
       if (!(error_reporting() & $errno)) {
           // This error code is not included in error_reporting, so let it fall
           // through to the standard PHP error handler
           return false;
       }
   
       switch ($errno) {
       case E_USER_ERROR:
           echo '<b>My ERROR</b> [$errno] $errstr<br />'.PHP_EOL;
           echo '  Fatal error on line '.$errline.' in file .'$errfile;
           echo ', PHP ' . PHP_VERSION . ' (' . PHP_OS . ')<br />'.PHP_EOL;
           echo 'Aborting...<br />'.PHP_EOL;
           exit(1);
           break;
   
       case E_USER_WARNING:
           echo '<b>My WARNING</b> ['.$errno.'] '.$errstr.'<br />'.PHP_EOL;
           break;
   
       case E_USER_NOTICE:
           echo '<b>My NOTICE</b> ['.$errno.'] '.$errstr.'<br />'.PHP_EOL;
           break;
   
       default:
           echo 'Unknown error type: ['.$errno.'] $errstr<br />'.PHP_EOL;
           break;
       }
   
       /* Don't execute PHP internal error handler */
       return true;
   }
   
   
   // set to the user defined error handler
   $old_error_handler = set_error_handler("myErrorHandler");
   
   ?>

See also `set_error_handler <http://www.php.net/set_error_handler>`_.

Connex PHP features
-------------------

  + `handler <https://php-dictionary.readthedocs.io/en/latest/dictionary/handler.ini.html>`_


Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Php/SetHandlers                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                            |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


