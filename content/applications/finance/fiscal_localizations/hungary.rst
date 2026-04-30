=======
Hungary
=======

.. _localizations_hungary/configuration/modules:

Modules
=======

The following modules are installed automatically with the Hungarian localization:

.. list-table::
   :header-rows: 1
   :widths: 25 25 50

   * - Name
     - Technical name
     - Description
   * - :guilabel:`Hungary - Accounting`
     - `l10n_hu`
     - Hungarian :ref:`fiscal localization package <fiscal_localizations/packages>`, complete with
       the Hungarian chart of accounts, taxes, tax report, and fiscal positions
   * - :guilabel:`Hungary - Accounting Reports`
     - `l10n_hu_reports`
     - Integration module of the Hungarian accounting reports
   * - :guilabel:`Hungary E-invoicing`
     - `l10n_hu_edi`
     - Integration module to support the Hungarian tax authority e-Invoicing (NAV 3.0) requirements

.. note::
   In some cases, such as when upgrading to a version with additional modules, it is possible that
   modules may not be installed automatically. Any missing modules can be manually :ref:`installed
   <general/install>`.

.. _localizations/hungarian/specifics:

Localization overview
=====================

The Hungarian localization package offers key features and integration capabilities that
collectively ensure compliance with local fiscal and accounting regulations. It includes tools for
managing taxes, fiscal positions, reporting, and a predefined chart of accounts tailored to
Hungarian authorities' standards.

- :doc:`../accounting/get_started/chart_of_accounts`: a predefined structure tailored to Hungarian
  accounting standards.
- :ref:`localizations/hungary/taxes`: pre-configured tax rates, including standard VAT, zero-rated,
  and exempt options.
- :doc:`../accounting/taxes/fiscal_positions`: automated tax adjustments based on customer or
  supplier registration status.
- :ref:`localizations/hungary/tax-reporting`: detailed overview of your net tax liability.
- :ref:`E-invoicing (NAV 3.0) <localizations/hungary/e-invoicing>`: integration for electronic
  invoicing in line with Hungarian government requirements.

.. _localizations/hungary/taxes:

Taxes
-----

The following :doc:`taxes <../accounting/taxes>` are available by default with the Hungarian
localization package:

- Standard sales tax (27%) and reduced rates (18%, 5%): applied to most goods and services within
  Hungary.
- Agricultural compensation surcharge (12%): applied to specific agricultural products.
- Intra-community taxes (0%), export taxes (0%), and specific exemptions (0%): applied to goods and
  services sold within the EU, exported outside of the EU, and specific tax exemption cases.

.. _localizations/hungary/tax-reporting:

Tax reporting
-------------

The :doc:`VAT summary <../accounting/reporting/tax_returns>` provides a detailed breakdown of
taxable, zero-rated, and exempt transactions. Like other :doc:`financial reports
<../accounting/reporting>`, the VAT summary can be filtered by period, compared against other
periods, and exported in Excel and PDF formats, ensuring compliance with Jordanian tax laws.

.. _localizations/hungary/e-invoicing:

e-Invoicing with NAV 3.0
========================

NAV 3.0 e-Invoicing is seamlessly integrated with Odoo to meet Hungarian authorities' technical and
legal requirements for electronic invoicing. With this integration, companies can:

- Generate compliant electronic invoices.
- Submit invoices in real time for validation.
- Track invoice statuses directly within Odoo.

Configuration
-------------

Link NAV 3.0 to Odoo
~~~~~~~~~~~~~~~~~~~~

To configure NAV 3.0 e-Invoicing, open the **Accounting** app, navigate to
:menuselection:`Configuration --> Settings`. Scroll to :guilabel:`Hungarian Electronic Invoicing`,
select the desired :guilabel:`Mode`, and enter the e-Invoicing credentials provided by the Hungarian
authorities. If applicable, also select the :guilabel:`NAV Tax Regime`.

Company and customers
---------------------

The NAV 3.0 invoicing workflow requires address information related to the company that sends the
invoices and the customers who receive them:

#. Go to :menuselection:`Settings --> Users & Companies --> Companies` and select the company that
   will use NAV 3.0.
#. Fill in the :guilabel:`Company Name`, :guilabel:`VAT` (TIN), and :guilabel:`Country`. If desired,
   fill in additional optional fields such as :guilabel:`Street`, :guilabel:`City`,
   :guilabel:`State`, and :guilabel:`ZIP`.

   .. Important::
      - The :guilabel:`Country` must be set to :guilabel:`Hungary`.
      - The :guilabel:`Company Name` must match the name that is registered with the ISTD (check for hungary)
      - The :guilabel:`VAT` can either be a European VAT number or Hungarian TIN number.
      - The company's :guilabel:`Currency` must be set to either :guilabel:`HUF` or :guilabel:`EUR`.

To send an invoice with NAV 3.0, open the invoice, click :guilabel:`Send`, check the
:guilabel:`NAV 3.0` option, and then click :guilabel:`Send` again to complete the process.

.. _localizations/hungary/storno-credit-notes:

Storno and credit notes
-----------------------

