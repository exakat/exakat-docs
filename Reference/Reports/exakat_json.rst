.. _report-exakat-json:

Exakat Json
+++++++++++

Exakat Json
___________

The Exakat JSON report exports in a flat JSON format.

Simple Json format. It is a flat array of objects, all with the same structure.

::

    [
      {
        "exakatVersion": "2.2.2",
        "exakatFingerprint": "f93c98ed693f29abc75b52154482ac4f6ff1b59b",
        "analyzedAt": "2021-09-10T16:59:20+00:00",
        "uuid": "1234567abcd",
        "project": "sculpin",
        "branch": "master",
        "lastCommitId": "b7c9027f05d9bff4dc6e92f36d29c4738bfc0b42",
        "ruleId": "Classes\\/ChildRemoveTypehint",
        "type": "warning",
        "severity": "major",
        "fixable": "fixable",
        "file": "\\/src\\/Sculpin\\/Core\\/Source\\/SourceInterface.php",
        "namespace": "\\sculpin\\core\\source",
        "class": "",
        "function": "",
        "message": "Child Class Removes Typehint",
        "startLine": 144,
        "endLine": 144,
        "fullCode": "public function duplicate(string $newSourceId) : SourceInterface ;",
      },
    
    ]



This Report may be configured with the [Exakatjson] section, to provide the uuid value.

::

    [Exakatjson]
    uuid="1234567abcd";




Specs
_____

+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Short name   | Exakat Json                                                                                                             |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Rulesets     | This reports works with an arbitrary list of results.                                                                   |
|              |                                                                                                                         |
|              |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Type         | Json                                                                                                                    |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Target       |                                                                                                                         |
+--------------+-------------------------------------------------------------------------------------------------------------------------+
| Available in | `Entreprise Edition <https://www.exakat.io/entreprise-edition>`_, `Exakat Cloud <https://www.exakat.io/exakat-cloud/>`_ |
+--------------+-------------------------------------------------------------------------------------------------------------------------+


