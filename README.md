password_strength
======================

This is a Drupal 8 module that adds a PasswordStrength plugin to the D8 Password Policy module. Implemented from https://github.com/bjeavons/zxcvbn-php

After developing this module, I was informed about the following module: https://www.drupal.org/project/password_strength. This module is basically a D8 version of the module that now plugs into Password Policy.

**Enable**

-  Download and enable the module
-  Go to Password Policy's configuration page (/admin/config/security/password/settings)
-  Click on the "Zxcvbn" tab
-  Click "Add Policy" and define select the score you wish to use
-  Go to the permissions page (/admin/people/permissions)
-  Select which roles the Zxcvbn policy applies to
-  Drink a beer

**Configure**

-  Go to Password Policy Zxcvbn's configuration page (/admin/config/security/zxcvbn/settings)
-  Turn on/off matchers
-  Select your scorer and searcher


**Architecture**

-  Base Zxcvbn class that bootstraps the code and the configured plugins
-  Three plugin managers for full extensibility: Matcher, Scorer, and Searcher
