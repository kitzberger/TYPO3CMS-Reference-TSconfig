.. include:: /Includes.rst.txt
.. index::
   TCAdefaults
   Records; Default values
.. _pageTsTcaDefaults:

===========
TCAdefaults
===========

This allows to set or override the `default` values of `TCA` fields that is available
for various TCA types, for instance for :ref:`type=input <t3tca:columns-input-properties-default>`.

The full path of a setting include the table and the field name: `TCAdefaults.[table name].[field]`

This key is also available on :ref:`User TSconfig level <userTsTcaDefaults>`, the order of default
values when creating new records in the backend is this:

#. Value from $GLOBALS['TCA']

#. Value from :ref:`User TSconfig <userTsTcaDefaults>`

#. Value from page TSconfig (these settings)

#. Value from "defVals" GET variables

#. Value from previous record based on 'useColumnsForDefaultValues'

Example:

.. code-block:: typoscript
   :caption: EXT:site_package/Configuration/page.tsconfig

   # Show newly created pages by default
   TCAdefaults.pages.hidden = 0
