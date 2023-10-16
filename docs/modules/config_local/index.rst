:py:mod:`config_local`
======================

.. py:module:: config_local

.. autoapi-nested-parse::

   autoread_dotenv.__init__.

   We assume following directory-structure:
   The virtualenv of your project **must** be created as a
   .venv-subfolder inside your project-directory.

   This corresponds to poetry-config "in-project = true".
   The .env-file must reside in the root of your project-directory.

   .. code-block:: python

     <project-root>
         .env
         .venv/
             bin/
                 python
             lib/
             lib64/
             pyvenv.cfg

     We also support toplevel-symlinks to the corresponding .venv-files:

   .. code-block:: python

         bin/       -> .venv/bin/
         lib/       -> .venv/lib/
         lib64/     -> .venv/lib64/
         pyvenv.cfg -> .venv/pyvenv.cfg



Package Contents
----------------

Classes
~~~~~~~

.. autoapisummary::

   config_local.SimpleWarning



Functions
~~~~~~~~~

.. autoapisummary::

   config_local.get_dotenv_path
   config_local.entrypoint



Attributes
~~~~~~~~~~

.. autoapisummary::

   config_local.__version__
   config_local.__copyright__
   config_local.__license__
   config_local.DOTENV_INSTALLED


.. py:data:: __version__
   :value: '1.0.3'

   

.. py:data:: __copyright__
   :value: 'Copyright 2023 Libranet'

   

.. py:data:: __license__
   :value: 'MIT License'

   

.. py:data:: DOTENV_INSTALLED
   :value: 1

   

.. py:class:: SimpleWarning


   Simple warning-formatting .

   .. py:method:: __enter__()

      Enter contextmanager.


   .. py:method:: __exit__(*args)

      Exit contextmanager.


   .. py:method:: simple_message(message, *args, **kwargs)
      :staticmethod:

      Return a simple warning-message without any traceback-info.



.. py:function:: get_dotenv_path()

   Return the location of the .env for in-project virtualenvs.

   Return None of the .env-file does not exist.


.. py:function:: entrypoint()

   Set environment-variable from the in-project .env-file.


