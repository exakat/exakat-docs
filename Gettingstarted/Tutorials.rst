.. _Tutorials:

Tutorials
*********

* :ref:`First audit with Exakat <first-audit-local>`
* :ref:`First audit with Exakat (Docker) <first-audit-docker>`
* :ref:`In the code auditing with Exakat <in-code-auditing-local>`
* `Prepare for PHP migration with Exakat <https://www.exakat.io/prepare-for-php-migration-with-exakat/>`_ (=> exakat.io)
* `Installing Exakat to monitor several projects <https://www.exakat.io/installing-exakat-to-monitor-several-projects/>`_ (=> exakat.io)

.. _first-audit-local:

First audit with Exakat
-----------------------

In this tutorial, we'll use an open source project called 'sculpin' as a guinea pig. You can replace it with any accessible source code of yours. The name of the project is also 'sculpin', though this is both self-descriptive and arbitrary. 

Init a project
################

::

	php exakat.phar doctor
	php exakat.phar init -p sculpin -R https://github.com/sculpin/sculpin.git

After this step, there is a folder 'sculpin' inside the 'projects' folder. The files will be stored there. 

Run exakat
##########

::

	php exakat.phar project -p sculpin -v

This command runs the default configuration over the requested code source. After displaying the different steps, it provides a first report: Diplomat.

Open the report, with a web browser: it is located in projects/sculpin/diplomat. 

Congratulations, this is your first audit.

.. _first-audit-docker:

First audit with Exakat (Docker)
--------------------------------

In this tutorial, we'll use an open source project called 'sculpin' as a guinea pig. You can replace it with any accessible source code of yours. The name of the project is also 'sculpin', though this is both self-descriptive and arbitrary. 

Init a project
################

::

    docker run -it -v $(pwd)/projects:/usr/src/exakat/projects --rm --name my-exakat exakat/exakat exakat init -p sculpin -R https://github.com/sculpin/sculpin.git

After this step, there is a folder 'sculpin' inside the 'projects' folder. The files will be stored there. 

::

    docker run -it -v /home/my-user/.ssh:/home/exakat/ssh -v $(pwd)/projects:/usr/src/exakat/projects --rm --name my-exakat exakat/exakat exakat project -p sculpin  -v


Run exakat
################

::

    docker run -it -v $(pwd)/projects:/usr/src/exakat/projects --rm --name my-exakat exakat/exakat exakat project -p sculpin -v

This command runs the default configuration over the requested code source. After displaying the different steps, it provides a first report: Diplomat.

Open the report, with a web browser: it is located in projects/sculpin/diplomat. 

Congratulations, this is your first audit.


.. _in-code-auditing-local:

In Code Auditing With Exakat (Local)
----------------------------------------

In this tutorial, we show how to run exakat within the code source itself, instead of running it with a separate folder. 

As a pre requisite, you should have installed Exakat on your system, and, in a different folder, hold some source code that needs to be audited.  

Init the project
################

Exakat recognizes the code as an auditable source code when it can find a ``.exakat.ini`` or ``.exakat.yaml`` file in the source.

The ``.exakat.yaml`` file : 

::

    project = "exakat";
    project_reports[] = "Text";


The ``.exakat.yaml`` file : 

:: 
---

    project: exakat
    project_reports:
      - Text

In case both files are found, the ``.INI`` file has precedence. 

Run exakat
################

::

    php /path/to/installation/exakat.phar project -v 

This command runs the default configuration over the code source. It displays immediately the audit as a Text file, directly in the terminal. 

Congratulations, this is your first audit.


.. _in-code-auditing-docker:

In Code Auditing With Exakat (Docker)
----------------------------------------

In this tutorial, we show how to run exakat within the code source itself, instead of running it with a separate folder. We'll use a Docker installation for that. 

As a pre requisite, you should have pulled the exakat/exakat:latest on your docker installation; and, in a different folder, hold some source code that needs to be audited.  

Init the project
################

Exakat recognizes the code as an auditable source code when it can find a ``.exakat.ini`` or ``.exakat.yaml`` file in the source.

The ``.exakat.yaml`` file : 

::

    project = "exakat";
    project_reports[] = "Text";


The ``.exakat.yaml`` file : 

:: 
---

    project: exakat
    project_reports:
      - Text

In case both files are found, the ``.INI`` file has precedence. 

Run exakat
###########

::

    docker run -it -v $(pwd):/src --rm --name my-exakat exakat/exakat exakat project 

This command runs the default configuration over the code source. It displays immediately the audit as a Text file, directly in the terminal. 

Congratulations, this is your first audit.
