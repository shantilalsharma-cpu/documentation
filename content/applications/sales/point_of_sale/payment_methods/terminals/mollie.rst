======
Mollie
======

**Mollie** is a payment service that offers payment solutions through physical :doc:`payment terminals <../terminals>`,
tap terminals, and terminal apps for Android and iOS devices.

.. note::
   Mollie payment terminals do not require an IoT Box to operate.

.. seealso::
   `List of supported countries <https://help.mollie.com/hc/en-us/articles/33911501243154-In-person-payments-supported-countries>`_

Mollie configuration
====================

To configure a Mollie terminal, create a `Mollie account <https://my.mollie.com>`_, then follow these steps:

#. Go to the :guilabel:`In-person payments` section in the left sidebar to access the list of terminals.
#. Select the desired payment terminal from the list.
#. Click the :guilabel:`Terminal information` tab in the top menu.
#. Copy the :guilabel:`Terminal ID` and keep it handy for the :ref:`Odoo POS configuration <pos/mollie/pos_configuration>` process.
#. Click the :guilabel:`Developers` icon in the bottom left corner.
#. Copy the :guilabel:`Live API key` and keep it handy for the :ref:`Odoo POS configuration <pos/mollie/pos_configuration>` process.

.. warning::
   Treat the :guilabel:`Live API key` as a password and keep it secure, as it provides access to your Mollie account.

.. note::
   To set up a Mollie terminal, find all the available options on the `Mollie website <https://www.mollie.com/products/pos-payments>`_.

.. _pos/mollie/pos_configuration:

Odoo POS configuration
======================

To connect the Mollie terminal with Odoo Point of Sale, follow these steps:

#. Go to :menuselection:`Point of Sale --> Configuration --> Payment Methods` and :doc:`create a
   payment method <../../payment_methods>`.
#. Set the :guilabel:`Journal` field to :guilabel:`Bank`.
#. Select the desired point of sale in the :guilabel:`Point of Sale` field.
#. Set the :guilabel:`Integration` field to :guilabel:`Terminal`.
#. Click :guilabel:`Activate` or :guilabel:`Setup` under the Mollie integration from the list of providers if needed.
#. Optionally, set the :guilabel:`Integrate with` field to :guilabel:`Mollie`.
#. Set the :guilabel:`Mollie Payment Provider` field to :guilabel:`Mollie`.
#. Paste the Terminal ID into the :guilabel:`Mollie Terminal ID` field.
#. Save the payment method.
#. Click the :icon:`fa-arrow-right` (:guilabel:`Internal link`) icon next to the :guilabel:`Mollie Payment Provider` field.
#. Paste the API key into the :guilabel:`API Key` field. Leave the :guilabel:`State` field
   on :guilabel:`Disabled` if the payment provider is not used for online payments.
#. Save the payment provider form.
