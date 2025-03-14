.. _translations:

Translations
============

Group-Office comes in many languages thanks to our community!

At the moment we have the following:

- Arabic عربي 
- বাংলা (Bangladesh)
- 한국어
- Bulgarian
- Català
- Chinese Simplified
- Chinese Traditional
- Čeština
- Dansk
- Deutsch
- English/American
- English/British
- Español
- Estonian
- Ελληνικά
- Francais
- Hrvatski
- Italiano
- Japanese
- Magyar
- Монгол хэл (Mongolian)
- Nederlands
- Norsk bokmål
- Polski
- Portugués - Portugal
- Português - Brazil
- Pусский
- Romanian
- Suomi - Finland
- Svenska
- Türkçe
- ไทย
- Tiếng Việt
- Български

Contribute
----------

We've made it easy for you to contribute to translations. We can export and import them using a CSV spreadsheet file._customize
You can make the translations and send it to support@intermesh.nl. Then we can import it into the project and
include it in the next release.

There are 3 options to obtain the spreadsheet:

1. You can find the **download spreadsheet** button next to the language selection in **System Settings -> General**.

2. You can request a spreadsheet from us at support@intermesh.nl with the missing translations. We use `LibreTransate <https://libretranslate.com>`_ to translate the missing entries. We ask you to verify these machine translations.

3. You can generate the spreadsheet with machine translations yourself using our `Docker development environment <https://github.com/Intermesh/docker-groupoffice-development>`_. See the "Translation" section.


.. note:: If you want to import the language CSV file yourself then install the Community / Developer tools module you
    and run the following command in a terminal:

    .. code::

        ./cli.php community/dev/Language/import --path=lang.csv

.. _customize-language:

Customize
---------

It's possible to customize language by overriding the default language string. For example if you want to rename "Address book" to "Contact" you create this file in the Admin personal file area::

   language/community/addressbook/en.php
   
So this is language/<MODULE PACKAGE>/<MODULE NAME>/<LANGCODE>.php

Enter this PHP code in the file::

   <?php
   return [
    "Address book" => "Contacts"
   ];
   
   
After placing the file run /install/upgrade.php to rebuild the server cache. Then check if the address book tab text changed into "Contacts".
   
