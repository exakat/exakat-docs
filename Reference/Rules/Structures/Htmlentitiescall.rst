.. _structures-htmlentitiescall:


.. _htmlentities-calls:

Htmlentities Calls
++++++++++++++++++

.. meta::
	:description:
		Htmlentities Calls: htmlentities() and htmlspecialchars() are used to prevent injecting special characters in HTML code.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: Htmlentities Calls
	:twitter:description: Htmlentities Calls: htmlentities() and htmlspecialchars() are used to prevent injecting special characters in HTML code
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: Htmlentities Calls
	:og:type: article
	:og:description: htmlentities() and htmlspecialchars() are used to prevent injecting special characters in HTML code
	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/Htmlentities Calls.html
	:og:locale: en

.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Htmlentitiescall.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Structures\/Htmlentitiescall.html","name":"Htmlentities Calls","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:18 +0000","dateModified":"Fri, 10 Jan 2025 09:46:18 +0000","description":"htmlentities() and htmlspecialchars() are used to prevent injecting special characters in HTML code","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/Htmlentities Calls.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

`htmlentities() <https://www.php.net/htmlentities>`_ and `htmlspecialchars() <https://www.php.net/htmlspecialchars>`_ are used to prevent injecting special characters in HTML code. As a bare minimum, they take a string and encode it for HTML.

The second argument of the functions is the type of protection. The protection may apply to quotes or not, to HTML 4 or 5, etc. It is highly recommended to set it explicitly.

The third argument of the functions is the encoding of the string. In PHP 5.3, it is ``ISO-8859-1``, in 5.4, was ``UTF-8``, and in 5.6, it is now default_charset, a ``php.ini`` configuration that has the default value of ``UTF-8``. It is highly recommended to set this argument too, to avoid distortions from the configuration.
Also, note that arguments 2 and 3 are constants and string, respectively, and should be issued from the list of values available in the manual. Other values than those will make PHP use the default values.

.. code-block:: php
   
   <?php
   $str = 'A quote is <b>bold</b>';
   
   // Outputs, without depending on the php.ini: A &#039;quote&#039; is &lt;b&gt;bold&lt;/b&gt; 
   echo htmlentities($str, ENT_QUOTES, 'UTF-8');
   
   // Outputs, while depending on the php.ini: A quote is &lt;b&gt;bold&lt;/b&gt;
   echo htmlentities($str);
   
   ?>

See also `htmlentities <https://www.php.net/htmlentities>`_ and `htmlspecialchars <https://www.php.net/htmlspecialchars>`_.

Connex PHP features
-------------------

  + `html-entity <https://php-dictionary.readthedocs.io/en/latest/dictionary/html-entity.ini.html>`_


Suggestions
___________

* Always use the third argument with htmlentities()




Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Structures/Htmlentitiescall                                                                                                                                                             |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CE <ruleset-CE>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`            |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Instant (5 mins)                                                                                                                                                                        |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule | :ref:`htmlentities-using-default-flag`                                                                                                                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


