.. _structures-htmlentitiescalldefaultflag:

.. _htmlentities-using-default-flag:

Htmlentities Using Default Flag
+++++++++++++++++++++++++++++++

  `htmlspecialchars() <https://www.php.net/htmlspecialchars>`_, `htmlentities() <https://www.php.net/htmlentities>`_, `htmlspecialchars_decode() <https://www.php.net/htmlspecialchars_decode>`_, `html_entity_decode() <https://www.php.net/html_entity_decode>`_ and `get_html_translation_table() <https://www.php.net/get_html_translation_table>`_, are used to prevent injecting special characters in HTML code. As a bare minimum, they take a string and encode it for HTML.

The second argument of the functions is the type of protection. The protection may apply to quotes or not, to HTML 4 or 5, etc. It is highly recommended to set it explicitly.

In PHP 8.1, the default value of this parameter has changed. It used to be ``ENT_COMPAT`` and is now ``ENT_QUOTES | `ENT_SUBSTITUTE <https://www.php.net/ENT_SUBSTITUTE>`_``. The main difference between the different configuration is that the single quote, which was left intact so far, is now protected HTML style.

.. code-block:: php
   
   <?php
   $str = 'A quote in <b>bold</b> : \' and ""';
   
   // PHP 8.0 outputs, without depending on the php.ini: A quote in &lt;b&gt;bold&lt;/b&gt; : ' and &quot;
   echo htmlentities($str);
   
   // PHP 8.1 outputs, while depending on the php.ini: A quote in &lt;b&gt;bold&lt;/b&gt; : &#039; and &quot;
   echo htmlentities($str);
   
   ?>

See also `htmlentities <https://www.php.net/htmlentities>`_ and `htmlspecialchars <https://www.php.net/htmlspecialchars>`_.

Connex PHP features
-------------------

  + `escape-sequence <https://php-dictionary.readthedocs.io/en/latest/dictionary/escape-sequence.ini.html>`_
  + `html-entity <https://php-dictionary.readthedocs.io/en/latest/dictionary/html-entity.ini.html>`_
  + `class <https://php-dictionary.readthedocs.io/en/latest/dictionary/class.ini.html>`_


Suggestions
___________

* Always use the second argument to explicitly set the desired protection




Specs
_____

+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name       | Structures/HtmlentitiescallDefaultFlag                                                                                                               |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets         | :ref:`All <ruleset-All>`, :ref:`Analyze <ruleset-Analyze>`, :ref:`CI-checks <ruleset-CI-checks>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>` |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since     | 2.2.3                                                                                                                                                |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version      | With PHP 8.1 and more recent                                                                                                                         |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity         | Minor                                                                                                                                                |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix      | Quick (30 mins)                                                                                                                                      |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Changed Behavior | PHP 8.1 - `More <https://php-changed-behaviors.readthedocs.io/en/latest/behavior/.html>`__                                                           |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision        | High                                                                                                                                                 |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Related rule     | :ref:`htmlentities-calls`                                                                                                                            |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in     | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_                              |
+------------------+------------------------------------------------------------------------------------------------------------------------------------------------------+


