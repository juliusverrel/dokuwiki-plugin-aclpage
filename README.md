Add ACL rules from wiki page and configuration settings
=======================================================

In addition to the ACL rules (usually) defined in conf/auth.acl.php, this plugin imports ACL rules from

* a wiki page (default: ``admin:add_acl``) defined in configuration manager (field: ``add_acl_page``)
* a multiline string (default: ``''``), defined in configuration manager (field: `add_acl`)

Moreover, additional placeholders (in addition to %GROUP% and %USER%) are defined for page ids: 

* ``%NAME%``: Full name of the user
* ``%EMAIL%``: Email address
* ``%EMAILNAME%``: "Name part" of email address (before @)
* ``%EMAILSHORT%``: "Name part" + some optional extra ("student" if @ ist followed by student)

The corresponding values are converted to valid dokuwiki page ids (by ``cleanID``).

