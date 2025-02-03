.. _extensions-extfann:


.. _ext-fann:

ext/fann
++++++++


.. meta::

	:description:

		ext/fann: Extension ``FANN`` : Fast Artificial Neural Network.

	:twitter:card: summary_large_image

	:twitter:site: @exakat

	:twitter:title: ext/fann

	:twitter:description: ext/fann: Extension ``FANN`` : Fast Artificial Neural Network

	:twitter:creator: @exakat

	:twitter:image:src: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:image: https://www.exakat.io/wp-content/uploads/2020/06/logo-exakat.png

	:og:title: ext/fann

	:og:type: article

	:og:description: Extension ``FANN`` : Fast Artificial Neural Network

	:og:url: https://exakat.readthedocs.io/en/latest/Reference/Rules/ext/fann.html

	:og:locale: en


.. raw:: html


	<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"WebPage","@id":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extfann.html","url":"https:\/\/php-tips.readthedocs.io\/en\/latest\/Reference\/Rules\/Extensions\/Extfann.html","name":"ext\/fann","isPartOf":{"@id":"https:\/\/www.exakat.io\/"},"datePublished":"Fri, 10 Jan 2025 09:46:17 +0000","dateModified":"Fri, 10 Jan 2025 09:46:17 +0000","description":"Extension ``FANN`` : Fast Artificial Neural Network","inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https:\/\/exakat.readthedocs.io\/en\/latest\/ext\/fann.html"]}]},{"@type":"WebSite","@id":"https:\/\/www.exakat.io\/","url":"https:\/\/www.exakat.io\/","name":"Exakat","description":"Smart PHP static analysis","inLanguage":"en-US"}]}</script>

Extension ``FANN`` : Fast Artificial Neural Network.

PHP binding for ``FANN`` library which implements multi-layer artificial neural networks with support for both fully connected and sparsely connected networks.

.. code-block:: php
   
   <?php
   $num_input = 2;
   $num_output = 1;
   $num_layers = 3;
   $num_neurons_hidden = 3;
   $desired_error = 0.001;
   $max_epochs = 500000;
   $epochs_between_reports = 1000;
   
   $ann = fann_create_standard($num_layers, $num_input, $num_neurons_hidden, $num_output);
   
   if ($ann) {
       fann_set_activation_function_hidden($ann, FANN_SIGMOID_SYMMETRIC);
       fann_set_activation_function_output($ann, FANN_SIGMOID_SYMMETRIC);
   
       $filename = dirname(__FILE__) . '/xor.data';
       if (fann_train_on_file($ann, $filename, $max_epochs, $epochs_between_reports, $desired_error))
           fann_save($ann, dirname(__FILE__) . '/xor_float.net');
   
       fann_destroy($ann);
   }
   ?>

See also `extension FANN <https://www.php.net/manual/en/book.fann.php>`_, `PHP-ML <https://php-ml.readthedocs.io/en/latest/>`_, `Rubix ML <https://rubixml.com/>`_ and `lib FANN <http://leenissen.dk/>`_.

Connex PHP features
-------------------

  + `machine-learning <https://php-dictionary.readthedocs.io/en/latest/dictionary/machine-learning.ini.html>`_


Specs
_____

+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Short name   | Extensions/Extfann                                                                                                                                                                      |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | :ref:`All <ruleset-All>`, :ref:`Appinfo <ruleset-Appinfo>`, :ref:`CE <ruleset-CE>`, :ref:`Changed Behavior <ruleset-Changed-Behavior>`                                                  |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Exakat since | 0.8.4                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| PHP Version  | All                                                                                                                                                                                     |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Severity     | Major                                                                                                                                                                                   |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Time To Fix  | Slow (1 hour)                                                                                                                                                                           |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Precision    | High                                                                                                                                                                                    |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Community Edition <https://www.exakat.io/community-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+


