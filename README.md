# Prestashop to Woocommerce migration
This repository is a migration of products and customer from Prestashop format to Woocommerce ready to import format. The file is written in Jupyter notebook. You can find the detail on this link.

### *I can't upload my data due to privacy of my customer.

## Product migration:

https://github.com/TrinVeerasiri/presta_to_woo_migration/blob/master/product.ipynb


## Customer migration:

I separate into 2 part
- Gathering customer information

  https://github.com/TrinVeerasiri/presta_to_woo_migration/blob/master/gathering_customer_information.ipynb
  
- Generate wp_users and wp_usermeta

  https://github.com/TrinVeerasiri/presta_to_woo_migration/blob/master/generate_wp_users_and_wp_usermeta.ipynb

## Product translation in English
This is the code for translation of products. In Prestashop, we have products in Thai and English description. We need to move the translation database to Woocommerce. Woocommerce uses "WPML Multilingual CMS" plugin. After activate, this plugin will create a database called "wp_icl_translation". The "trid" column is used to match the Thai and English version of the same product. 

Our process is to create a English description product in "wp_posts" and "wp_postmeta" then match the "trid" of Thai and English product in "wp_icl_translations".

https://github.com/TrinVeerasiri/presta_to_woo_migration/blob/master/translation.ipynb

## Add users nicename
After the web opening, admin tells the user that they have to change the password because we don't migrate them from Prestashop. The problem is old users don't have a user nicename, so they can't change their password. We solve this problem by copy the information of "user_login" column to fill nan values in "user_nicename" column of wp_post_meta.
https://github.com/TrinVeerasiri/presta_to_woo_migration/blob/master/add_user_nicename.ipynb
