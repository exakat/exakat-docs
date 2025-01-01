.. _extensions-extgettext:

.. _ext-gettext:

ext/gettext
+++++++++++

.. meta::
	:description:
		ext/gettext: Extension Gettext.
	:twitter:card: summary_large_image
	:twitter:site: @exakat
	:twitter:title: ext/gettext
	:twitter:description: ext/gettext: Extension Gettext
	:twitter:creator: @exakat
	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png
	:og:title: ext/gettext
	:og:type: article
	:og:description: Extension Gettext
	:og:url: https://php-tips.readthedocs.io/en/latest/tips/Extensions/Extgettext.html
	:og:locale: en
Extension Gettext.

The gettext functions implement an NLS (Native Language Support) API which can be used to internationalize your PHP applications.

.. code-block:: php
   
   <?php
   // Set language to German
   putenv('LC_ALL=de_DE');
   setlocale(LC_ALL, 'de_DE');
   
   // Specify location of translation tables
   bindtextdomain('myPHPApp', './locale');
   
   // Choose domain
   textdomain('myPHPApp');
   
   // Translation is looking for in ./locale/de_DE/LC_MESSAGES/myPHPApp.mo now
   
   // Print a test message
   echo gettext('Welcome to My PHP Application');
   
   // Or use the alias _() for gettext()
   echo _('Have a nice day');
   ?>

See also `Gettext <https://www.gnu.org/software/gettext/manual/gettext.html>`_ and `ext/gettext <https://www.php.net/manual/en/book.gettext.php>`_.


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extgettext                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  |                                                                                                                                                                                         |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | Very high                                                                                                                                                                               |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


