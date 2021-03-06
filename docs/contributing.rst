Contributing
============

Install Develop Version
-----------------------

To install Tianshou in an "editable" mode, run

.. code-block:: bash

    pip3 install -e .

in the main directory. This installation is removable by

.. code-block:: bash

    python3 setup.py develop --uninstall

Additional dependencies for developments can be installed by

.. code-block:: bash

    pip3 install ".[dev]"

PEP8 Code Style Check
---------------------

We follow PEP8 python code style. To check, in the main directory, run:

.. code-block:: bash

    flake8 . --count --show-source --statistics

Test Locally
------------

This command will run automatic tests in the main directory

.. code-block:: bash

    pytest test --cov tianshou -s --durations 0 -v

Test by GitHub Actions
----------------------

1. Click the ``Actions`` button in your own repo:

.. image:: _static/images/action1.jpg
    :align: center

2. Click the green button:

.. image:: _static/images/action2.jpg
    :align: center

3. You will see ``Actions Enabled.`` on the top of html page.

4. When you push a new commit to your own repo (e.g. ``git push``), it will automatically run the test in this page:

.. image:: _static/images/action3.png
    :align: center

Documentation
-------------

Documentations are written under the ``docs/`` directory as ReStructuredText (``.rst``) files. ``index.rst`` is the main page. A Tutorial on ReStructuredText can be found `here <https://pythonhosted.org/an_example_pypi_project/sphinx.html>`_.

API References are automatically generated by `Sphinx <http://www.sphinx-doc.org/en/stable/>`_ according to the outlines under ``docs/api/`` and should be modified when any code changes.

To compile documentation into webpages, run

.. code-block:: bash

    make html

under the ``docs/`` directory. The generated webpages are in ``docs/_build`` and can be viewed with browsers.
