=== yoonde ===
Contributors: Chris Ahrweiler
Tags: yoonde
Requires at least: 4.5
Stable tag: 1.0.1
Tested up to: 5.4.2
License: GPL2
License URI: https://www.gnu.org/licenses/gpl-2.0.html

== SubTitle ==

yoonde-API for WooCommerce

== Description ==

Plugin to access the yoonde-API and create yoonde-Token automatically on "woocommerce_order_status_completed"

== Installation ==

1. Upload the plugin folder to the `/wp-content/plugins/` directory or upload the zip within WordPress
2. Activate the plugin through the `Plugins` menu in WordPress
3. Configure the options under: `yoonde`

== 3rd Party or external service ==

This plugin uses the external API https://yoonde.de/api.php.
You will need an yoonde-API Token to access the API. 

In return this plugin will
1. Request all tokens, that you have created on the yoonde-platform, and list them on the plugin page.
2. Listen to the "woocommerce_order_status_completed" event and send a CREATE command to the yoonde-API, which will in return create a new token.

When sending the CREATE command, additional WooCommerce transaction data will be send to the API: get_billing_first_name, get_billing_last_name, get_billing_email and the yoonde parameters get_attribute('yoonde_category') and get_attribute('yoonde_chunks').

== Upgrade Notice ==

= 1.0 [2020.06.28] =
* Initial Release

= 1.0.1 [2020.07.02] =
Changes required by WP team.
- Using wp_enqueue commands
- Using HTTP API
- Documenting 3rd Party or external service
