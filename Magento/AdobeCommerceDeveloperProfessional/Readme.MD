### Creating a module
1. Create the module folder
   - app/code/Company/ModuleName/
     - cloning from github
     - for specific projects where code is committed to the projects repo directly
   - vendor/magento
     - composer installations
     - for modules that will be reused by multiple installations
2. Create the etc/module.xml file
    - Module name
      - <module name="Company_ModuleName" 
   - Module version
     - setup_version="0.0.1">
    - Module load order for dependencies
       - \<sequence>\<module name="Magento_Catalog" /> \</sequence>
3. Create the registration.php file
```
<?php

use Magento\Framework\Component\ComponentRegistrar;

ComponentRegistrar::registrer(type: ComponentRegistrar::MODULE, componentName: 'Company_ModuleName', path:__DIR__);
```
4.  Optional: composer.json file
    - Provide dependencies 
5.  Readme.MD
    - Provide documentation
5.  Run bin/magento setup:upgrade
6.  bin/magento module:enable Company_Module
### Module Structure
## Files
```
app/code/Company/ModuleName/etc/module.xml
```
- Register the name of the module

