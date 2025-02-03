.. _security-sessionlazywrite:

.. _session-lazy-write:

Session Lazy Write
++++++++++++++++++

.. meta::
	:description:
		Session Lazy Write: Classes that implements SessionHandlerInterface must also implements SessionUpdateTimestampHandlerInterface.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Session Lazy Write
	:twitter:description: Session Lazy Write: Classes that implements SessionHandlerInterface must also implements SessionUpdateTimestampHandlerInterface
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Session Lazy Write
	:og:type: article
	:og:description: Classes that implements SessionHandlerInterface must also implements SessionUpdateTimestampHandlerInterface
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Session Lazy Write.html
	:og:locale: en
.. raw:: html	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/SessionLazyWrite.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Security\/SessionLazyWrite.html","name":"Session Lazy Write","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"Classes that implements SessionHandlerInterface must also implements SessionUpdateTimestampHandlerInterface","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Session Lazy Write.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>Classes that implements `SessionHandlerInterface <https://www.php.net/sessionhandlerinterface>`_ must also implements `SessionUpdateTimestampHandlerInterface <https://www.php.net/sessionupdatetimestamphandlerinterface>`_. 

The two extra methods are used to help lazy loading : the first actually checks if a sessionId is available, and the seconds updates the time of last usage of the session data in the session storage. 

This was spotted by ``Nicolas Grekas``, and fixed in Symfony `[HttpFoundation] Make sessions `secure <https://www.php.net/secure>`_ and lazy #24523 <https://github.com/symfony/symfony/pull/24523>`_.

.. code-block:: php
   
   <?php
   
   interface SessionUpdateTimestampHandlerInterface {
       // returns a boolean to indicate that valid data is available for this sessionId, or not.
       function validateId($sessionId);
       
       //called to change the last time of usage for the session data.
       //It may be a file's touch or full write, or a simple update on the database
       function updateTimestamp($sessionId, $sessionData);
   }
   
   ?>

See also `Sessions: Improve original RFC about lazy_write <https://wiki.php.net/rfc/session-read_only-lazy_write>`_ and `Sessions <https://www.php.net/manual/en/book.session.php>`_.

Connex PHP features
-------------------

  + `session <https://php-dictionary.readthedocs.io/en/latest/dictionary/session.ini.html>`_


Suggestions
___________

* Implements the SessionUpdateTimestampHandlerInterface interface




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security/SessionLazyWrite                                                                                               |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`, :ref:`Security <ruleset-Security>`        |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.12.15                                                                                                                 |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                     |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                   |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


