# odoo_clouder_install
Automated install scripts for Odoo + Clouder. /!\ BETA version, do NOT use in production!
This scripts just needs to be preconfigured before being launched, no interaction needed. 

The script is based on the install scripts from André Schenkels (https://github.com/aschenkels-ictstudio/openerp-install-scripts), Yenthe (https://github.com/Yenthe666/InstallScript), Gustavo Valverde (https://github.com/gustavovalverde/odoo-install-scripts) with some additions from Nils Hamerlinck (http://nils.hamerlinck.fr/blog/2015/04/09/install-odoo-vps-ubuntu/)

It also follows the approach recommended in Odoo's documentation (https://www.odoo.com/documentation/9.0/setup/install.html) using pip instead of apt-get for python dependencies

> It's recommended to install this script with **elevated privileges**, so there's no need to use **sudo** to execute this procedure.

<h3>Installation procedure</h3>
1.  Download the script
  ```bash
  wget https://raw.githubusercontent.com/openexpertiz/InstallScript/master/odoo_clouder_install.sh
  ```

2.  **THIS IS IMPORTANT!** Modify this variables, otherwise you might get hacked too easily
  ```bash
    OE_USER="odoo"
    OE_SUPERADMIN="admin-OE2017"
  ```

3.  Modify this variables based on your needs
  ```bash
    INSTALL_CLOUDER="True"
    INSTALL_WKHTMLTOPDF="True"
    HAVE_PROXY="False" 
    OE_PORT="8069"
    OE_VERSION="8.0"
    IS_ENTERPRISE="False"
```

4.  Make the script executable
  ```bash
  chmod +x odoo_clouder_install.sh
  ```

5. Execute the script:
  ```bash
  . odoo_clouder_install.sh
  ```
