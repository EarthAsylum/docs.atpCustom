## ATP Custom Plugin for WordPress  
[![EarthAsylum Consulting](https://img.shields.io/badge/EarthAsylum-Consulting-0?&labelColor=6e9882&color=707070)](https://earthasylum.com/)
[![WordPress](https://img.shields.io/badge/WordPress-Plugins-grey?logo=wordpress&labelColor=blue)](https://wordpress.org/plugins/search/EarthAsylum/)
[![eacDoojigger](https://img.shields.io/badge/Requires-%7Beac%7DDoojigger-da821d)](https://eacDoojigger.earthasylum.com/)

<details><summary>Plugin Header</summary>

Plugin URI:             https://earthasylum.github.io/docs.atpCustom/  
Author:                 [EarthAsylum Consulting](https://www.earthasylum.com)  
Stable tag:             4.2.10-RC1+May10  
Last Updated:           10-May-2024  
Requires at least:      5.8  
Tested up to:           6.5  
WC requires at least:   7.0  
WC tested up to:        8.8  
Requires EAC:           2.5  
Requires PHP:           7.4  
Contributors:           [earthasylum](https://github.com/earthasylum),[kevinburkholder](https://profiles.wordpress.org/kevinburkholder)  
License:                Proprietary  
GitHub URI:             https://github.com/EarthAsylum/atpCustom  

</details>

> Adds WooCommerce customization, Cybersource gateway + NetSuite integration, Tealium, Bazaarvoice, Nuance chat, Facebook & Snapchat conversion, Kinsta API + more

### Description

**American Telecast Products plugin & extensions**

Adds WooCommerce customization, Cybersource gateway + NetSuite integration, Tealium, Bazaarvoice, Nuance chat, Facebook & Snapchat conversion, Kinsta API + more
    
#### Included Extensions

General / Tools

    ajaxAction.extension.php
    admin_tools.extension.php
    avatax.debugging.extension.php
    cart.debugging.extension.php
    encryption.extension.php
    session.extension.php

Code Injection

    inject_CSS.extension.php
    inject_HTML.extension.php
    inject_JS.extension.php
    inject_PHP.extension.php

Kinsta

    kinsta.extension.php

Marketing

    nuance_chat.extension.php
    offer_manager.extension.php
    offer_manager.taxonomy.php
    sourcing.extension.php

Order Processing

    cybersource.extension.php
    netscore.extension.php
    order_validation.extension.php
    salesorder_api.extension.php

Tracking

    bazaarvoice.extension.php
    facebook.extension.php
    snapchat.extension.php
    tealium.extension.php

Woocommerce

    cart.extension.php
    woocommerce.extension.php


#### Using atpCustom

atpCustom provides many useful methods which can be accessed from other custom plugins, extensions, or code snippets, as well as from template functions or any code in WordPress.

__Method Access__

Public methods in atpCustom may be accessed by using the global `ATP()` function.

    ATP()->{methodName}(...$arguments);

For example, to write an entry to the debugging log...

    ATP()->logDebug($myVariable,'Logging myVariable');

To access a plugin option...

    ATP()->get_option('my_option_name');

To execute a plugin action...

    ATP()->do_action('my_action_name',$arg1,$arg2,...);

To execute a method in a plugin extension, use `callMethod()`...

    ATP()->callMethod( [extensionName, extensionMethodName], ...$arguments )
    ATP()->extensionName->extensionMethodName( ...$arguments )

__How To__

Get a post value and format it using a shortcode

    [atpCustom method='get_the_field' args='_price, 2804, wc_price']

Get the current sourcing array using a filter

    $sourcing = $this->apply_filters( 'get_sourcing', [] );

Get the url "key" from sourcing using a filter

    $key = $this->apply_filters( 'get_sourcing', '', 'urlkey' );

Get the url "key" from sourcing using a shortcode

    [atpCustom method='getVariable' args='urlkey']

Get the current offer array using a filter

    $offer = $this->apply_filters( 'get_offer', [] );

Get the current offer name using a shortcode

    [atpCustom method='getVariable' args='OfferName']


>   __ATP Custom__ provides the same filters, shortcodes, and methods as {eac}Doojigger. See [Using {eac}Doojigger](https://eacdoojigger.earthasylum.com/using-doojigger/) for more.


### Installation

#### Automatic Plugin Installation

Due to the nature of this plugin, it is NOT available from the WordPress Plugin Repository and can not be installed from the WordPress Dashboard » *Plugins* » *Add New* » *Search* feature.

#### Upload via WordPress Dashboard

Installation of this plugin can be managed from the WordPress Dashboard » *Plugins* » *Add New* page. Click the [Upload Plugin] button, then select the atpCustom.zip file from your computer.

See [Managing Plugins -> Upload via WordPress Admin](https://wordpress.org/support/article/managing-plugins/#upload-via-wordpress-admin)

#### Manual Plugin Installation

You can install the plugin manually by extracting the atpCustom.zip file and uploading the 'atpCustom' folder to the 'wp-content/plugins' folder on your WordPress server.

See [Managing Plugins -> Manual Plugin Installation](https://wordpress.org/support/article/managing-plugins/#manual-plugin-installation-1)

#### Activation

On activation, custom tables and default settings/options are created. Be sure to visit the 'Settings' page to ensure proper configuration.

#### Updates

Updates are managed from the WordPress Dashboard » 'Plugins' » 'Installed Plugins' page. When a new version is available, a notice is presented under this plugin. Clicking on the 'update now' link will install the update; clicking on the 'View details' will provide more information on the update from which you can click on the 'Install Update Now' button.

When updated, any custom tables and/or option changes are applied. Be sure to visit the 'Settings' page.

#### Deactivation

On deactivation, the plugin makes no changes to the system but will not be loaded until reactivated.

#### Uninstall

When uninstalled, the plugin will delete custom tables, settings, and transient data based on the options selected in the general settings. If settings have been backed up, the backup is retained and can be restored if/when re-installed. Tables are not backed up.


### Other Notes

_atpCustom_ is an [{eac}Doojigger](https://eacDoojigger.earthasylum.com/) derivative and requires installation, activation, and registration of the {eac}Doojigger plugin.

#### Links

[Github Docs Page](https://github.com/EarthAsylum/docs.atpCustom)

[PHP Reference](https://earthasylum.github.io/docs.atpCustom/)


### Upgrade Notice

Requires {eac}Doojigger version 2.5+


