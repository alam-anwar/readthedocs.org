Importing your documentation
============================

.. meta::
   :description lang=en: Import your existing technical documentation from version control into Read the Docs.


To import a public documentation repository, visit your `Read the Docs dashboard`_ and click Import_.
For private repositories, please use :doc:`Read the Docs for Business </commercial/index>`.

Automatically import your docs
------------------------------

If you have :doc:`connected your Read the Docs account </guides/connecting-git-account>` to GitHub, Bitbucket, or GitLab,
you will see a list of your repositories that we are able to import.
To import one of these projects, just click the import
icon next to the repository you'd like to import. This will bring up a form that
is already filled with your project's information. Feel free to edit any of
these properties, and then click **Next** to
:ref:`build your documentation <intro/import-guide:Building your documentation>`.

.. _Read the Docs dashboard: https://readthedocs.org/dashboard
.. _Import: https://readthedocs.org/dashboard/import


.. figure:: ../_static/images/first-steps/import-a-repository.png
    :align: right
    :figwidth: 300px

    Importing a repository


Manually import your docs
-------------------------

If you have not :doc:`connected a Git provider account </guides/connecting-git-account>`,
you will need to select **Import Manually**
and enter the information for your repository yourself. You will also need to
manually configure the webhook for your repository as well. When importing your
project, you will be asked for the repository URL, along with some other
information for your new project. The URL is normally the URL or path name you'd
use to checkout, clone, or branch your repository. Some examples:

* ``https://github.com/ericholscher/django-kong.git``
* ``https://gitlab.com/gitlab-org/gitlab``

Add an optional homepage URL and some tags, and then click **Next**.

Once your project is created, you'll need to manually configure the repository
webhook if you would like to have new changes trigger builds for your
project on Read the Docs. Go to your project's :guilabel:`Admin` > :guilabel:`Integrations` page to
configure a new webhook.

.. seealso::

   :doc:`/guides/setup/git-repo-manual`
      Once you have imported your git project, use this guide to manually set up basic and additional *webhook* integration.

.. note::
    The ``Admin`` page can be found at ``https://readthedocs.org/dashboard/<project-slug>/edit/``.
    You can access all of the project settings from the admin page sidebar.

    .. figure:: ../_static/images/first-steps/admin-panel.png
        :figwidth: 400px


Building your documentation
---------------------------

Within a few seconds of completing the import process,
your code will automatically be fetched from your repository,
and the documentation will be built.
Check out our :doc:`/builds` page to learn more about how Read the Docs builds your docs,
and to troubleshoot any issues that arise.

We require an additional configuration file to build your project.
This allows you to specifying special requirements for your build,
such as your version of Python or how you wish to install addition Python requirements.
You can configure these settings in a ``.readthedocs.yaml`` file.
See our :doc:`/config-file/index` docs for more details.

.. note::

   Using a configuration file :doc:`is required from September 2023 <rtd-blog:migrate-configuration-v2>`.

It is also important to note that the default version of Sphinx is ``v1.8.5``.
We recommend to set the version your project uses :doc:`explicitily with pinned dependencies </guides/reproducible-builds>`.

Read the Docs will host multiple versions of your code. You can read more about
how to use this well on our :doc:`/versions` page.

If you have any more trouble, don't hesitate to reach out to us.
The :doc:`/support` page has more information on getting in touch.
