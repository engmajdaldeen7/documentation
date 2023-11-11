===========================
Set up your barcode scanner
===========================

.. _barcode/setup/hardware:

Follow this guide to choose and set up a barcode scanner compatible with Odoo's *Inventory* and
*Barcode* apps.

.. image:: hardware/barcode-scanner.png
   :align: center
   :alt: An image of an example barcode scanner.

Scanner types
=============

Before setting up a barcode scanner, it is important to determine which scanner type best meets the
needs of the business. There are three main types, each with their own benefits and use cases

- **USB scanners** are connected to a computer and are suitable for businesses that scan products at
  a fixed location, like at the checkout in a grocery store. Ensure the chosen USB scanner is
  compatible with the keyboard layout of the computer.

- **Bluetooth scanners** pair with a smartphone or tablet, making them an ideal cost-effective and
  portable barcode scanner option. In this scenario, Odoo is installed on the smartphone, allowing
  warehouse operators to handle operations and check stock directly through their mobile devices.

- **Mobile computer scanners** are mobile devices with a built-in barcode scanner. Ensure the device
  can run the Odoo mobile app properly. Recent models that use Android OS with the Google Chrome
  browser or Windows OS with Internet Explorer Mobile should work. However, testing is crucial due
  to the variety of available models and configurations.

Configuration
=============

When setting up the barcode scanner, ensure the following configurations are correctly set to ensure
the scanner can interpret barcodes properly in Odoo.

Keyboard layout
---------------

When using a USB barcode scanner, match its keyboard layout with the operating system's layout for
proper interpretation of characters. Generally, the scanning mode should be set to accept a USB
Keyboard (HID), with the language set based on the keyboard that is in use.

When configuring the keyboard layout for a Zebra scanner, scan the keyboard wedge barcode in the
user manual for the barcode scanner.

.. image:: hardware/keyboard-barcode.png
   :align: center
   :alt: Example of a user manual for keyboard layout.

Automatic carriage return
-------------------------

Odoo has a default 50-millisecond delay between scans to prevent accidental double scanning. To
synchronize with the barcode scanner, set it to include a *carriage return* (:dfn:`character like
the "Enter" key on a keyboard`) after each scan. Odoo interprets the carriage return as the end of
the barcode input; so Odoo accepts the scan and waits for the next one.

Typically, on the scanner, a carriage return is included by default. Ensure it is set by scanning a
specific barcode in the user manual, like 'CR suffix ON' or 'Apply Enter for suffix.'

Zebra scanner
-------------

When using Zebra scanners, ensure the correct keystroke configurations are set to prevent errors.

Begin on the Zebra scanner's home screen and select the :guilabel:`DataWedge` app (the icon for the
app is a light blue barcode). On the :guilabel:`DataWedge Profiles` page, select the profile option
to access the Zebra scanner's settings.

Scroll down to the :guilabel:`Keyboard Output` option and ensure the option
:guilabel:`Enable/disable keystroke output` is :guilabel:`Enabled`.

.. image:: hardware/enable-keystroke.png
   :align: center
   :alt: Show keystroke option in the Zebra scanner's DataWedge app.

Now, go back to the :guilabel:`Profile` options page and select :guilabel:`Key event options`. Here,
ensure the :guilabel:`Send Characters as Events` option is checked.
