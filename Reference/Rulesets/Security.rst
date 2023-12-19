.. _ruleset-security:

Security
++++++++

This ruleset focuses on code security. 

Total : 47 analysis

* :ref:`eval()-usage`
* :ref:`phpinfo`
* :ref:`var\_dump()...-usage`
* :ref:`hardcoded-passwords`
* :ref:`direct-injection`
* :ref:`avoid-sleep()-usleep()`
* :ref:`parse\_str()-warning`
* :ref:`avoid-those-hash-functions`
* :ref:`no-hardcoded-port`
* :ref:`should-use-prepared-statement`
* :ref:`no-hardcoded-ip`
* :ref:`compare-hash`
* :ref:`preg\_replace-with-option-e`
* :ref:`eval()-without-try`
* :ref:`register-globals`
* :ref:`safe-curl-options`
* :ref:`use-random\_int()`
* :ref:`no-hardcoded-hash`
* :ref:`random-without-try`
* :ref:`indirect-injection`
* :ref:`unserialize-second-arg`
* :ref:`don't-echo-error`
* :ref:`should-use-session\_regenerateid()`
* :ref:`encoded-simple-letters`
* :ref:`set-cookie-safe-arguments`
* :ref:`no-return-or-throw-in-finally`
* :ref:`mkdir-default`
* :ref:`switch-fallthrough`
* :ref:`upload-filename-injection`
* :ref:`always-anchor-regex`
* :ref:`session-lazy-write`
* :ref:`sqlite3-requires-single-quotes`
* :ref:`no-net-for-xml-load`
* :ref:`dynamic-library-loading`
* :ref:`configure-extract`
* :ref:`move\_uploaded\_file-instead-of-copy`
* :ref:`filter\_input()-as-a-source`
* :ref:`safe-http-headers`
* :ref:`insecure-integer-validation`
* :ref:`minus-one-on-error`
* :ref:`no-ent\_ignore`
* :ref:`no-weak-ssl-crypto`
* :ref:`keep-files-access-restricted`
* :ref:`check-crypto-key-length`
* :ref:`incompatible-types-with-incoming-values`
* :ref:`filter-not-raw`
* :ref:`unvalidated-data-cached-in-session`

Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Security                                                                                                                |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Reports      | :ref:`report-ambassador`, :ref:`report-owasp`                                                                           |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


