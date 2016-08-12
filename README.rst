Clouder - Hosting your Apps with Docker and Odoo
------------------------------------------------

`Clouder`_ is a platform which aims to standardize best practices for hosting open-source software. Whether you are launching a hosting offer, are the sysadmin of a company, or just want to host software for you and your friends, Clouder will allow you to easily deploy and maintain a professionnal infrastructure with very basic technical knowledge.

More specifically, Clouder is an orchestrator which is based on the Docker container technology. Each application will be installed inside a container and Clouder will establish links between them. 

Clouder is based on Odoo, an open-source software application which is very efficient at managing this kind of workflow and process.

Odoo - From ERP to CRM, eCommerce to CMS
----------------------------------------

`Odoo`_ is an all-in-one business management suite of mobile-friendly web apps that integrates everything you need to grow your business: CRM, website content management, project management, human resources, accounting, invoicing and more. Odoo apps integrate seamlessly to provide a full-featured open source ERP, but can also be used stand-alone.

odoo_clouder_install
====================
Automated install scripts for Odoo + Clouder:
- Odoo v8/v9 installed from upstream GIT source (`GitHub/Odoo`_)
- Clouder v8.1 installed from upstream GIT source (`GitHub/Clouder`_)
- Includes all base modules from base install of Odoo and Clouder
/!\\ BETA version, do NOT use in production! 

This scripts just needs to be preconfigured before being launched, no interaction needed. 

The script is based on the install scripts from André Schenkels (https://github.com/aschenkels-ictstudio/openerp-install-scripts), Yenthe (https://github.com/Yenthe666/InstallScript), Gustavo Valverde (https://github.com/gustavovalverde/odoo-install-scripts) with some additions from Nils Hamerlinck (http://nils.hamerlinck.fr/blog/2015/04/09/install-odoo-vps-ubuntu/)

It also follows the approach recommended in Odoo's documentation (https://www.odoo.com/documentation/9.0/setup/install.html) using pip instead of apt-get for python dependencies

 It's recommended to install this script with **elevated privileges**, so there's no need to use **sudo** to execute this procedure.

Installation procedure
======================
1.  Download the script:

``wget https://raw.githubusercontent.com/openexpertiz/InstallScript/master/odoo_clouder_install.sh``

2.  **This is important!** Modify this variables, otherwise you might get hacked too easily:

``OE_USER="odoo"``

``OE_SUPERADMIN="admin-OE2017"``

3.  Modify this variables based on your needs:

``INSTALL_CLOUDER="True"``
 
``INSTALL_WKHTMLTOPDF="True"``
 
``HAVE_PROXY="False"``
 
``OE_PORT="8069"``
 
``OE_VERSION="8.0"``
 
``IS_ENTERPRISE="False"``

4.  Make the script executable:

``chmod +x odoo_clouder_install.sh``

5. Execute the script:

``. odoo_clouder_install.sh``

.. _Odoo: https://www.odoo.com/
.. _Clouder: https://goclouder.net/
.. _GitHub/Odoo: https://github.com/odoo/odoo
.. _GitHub/Clouder: https://github.com/clouder-community/clouder
