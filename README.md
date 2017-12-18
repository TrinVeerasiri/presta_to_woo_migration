# Prestashop to Woocommerce migration
This repository is a migration of products and customer from Prestashop format to Woocommerce ready to import format. The file is written in Jupyter notebook. You can find the detail on this link.

1) The product migration:

https://github.com/TrinVeerasiri/presta_to_woo_migration/blob/master/product.ipynb


2) The customer migration:

I separate into 2 part
- Gathering customer information

  https://github.com/TrinVeerasiri/presta_to_woo_migration/blob/master/gathering_customer_information.ipynb
  
- Generate wp_users and wp_usermeta

  https://github.com/TrinVeerasiri/presta_to_woo_migration/blob/master/generate_wp_users_and_wp_usermeta.ipynb

3) Product translation in English
This is the code for translation of products. In Prestashop, we have products in Thai and English description. We need to move the translation database to Woocommerce. Woocommerce uses "WPML Multilingual CMS" plugin. After activate, this plugin will create a database called "wp_icl_translation". The "trid" column is used to match the Thai and English version of the same product. 

Our process is to create a English description product in "wp_posts" and "wp_postmeta" then match the "trid" of Thai and English product in "wp_icl_translations".

There are 3 parts.

3.1) Creating the "wp_posts" for English description products.

3.2) Creating the "wp_postmeta" for English description products.

3.3) Matching the "trid" of Thai and English product in the "wp_icl_translations"
