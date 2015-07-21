#Altitude Bootstrap

This compiled styles and javascript library is a development SCSS bootstrap for style and function development within the Altitude-Sports web sites. 

> Contains seperate scss files for ui and global elements
> seperated into unique callable css properties. 
> Uses a normalized grid system.
> Function based jQuery plugins.
> Minified JS output

###Version 

1.0.1

###Project Structure
```sh

- project root
    - assets
        - css (output non-distribution)
        - fonts (required bootstrap and iso fonts)
        - js (main altitude.js and minified files)
        - json (unuesed)
        - less (less compiled stylesheet)
        - sass (sass compiled css project)
        - scss (main css file directory)
            - base
                - collaborate (collaborative commons directory)
                - demo (base demo stylesheet)
                - objects
                - required
                    - functions
                    - mixins
                    - settings
                    - variables
                        - buttons
                        - colors
                - ui
                    - components
                        - blocks
                        - buttons
                        - dialogs
                        - form
                        - navigation-bar
                        - popovers
                        - tab-bar
                    - elements
    - dist (distribution directory)
        - compiled (compiled output)
        - demo
            - css
            - objects
            - ui
                - components
                    - blocks
                    - buttons
                    - dialogs
                    - form
                    - navigation-bar
                    - popovers
                    - tab-bar
                - effects
    - src
        - ionicons-2.0.1
        - jquery
        
```
        
###Project Compilation
Add or remove required files and components by including them in the globals.scss file. Set the output directory to dist -> compiled.

###Extending The Bootstrap
Add a working folder root to the scss -> collaborate folder (i.e. my-element) and create a compiler-ignored scss file containing custom styling classes (i.e. _my-new-element.scss). 
> Add the new files to the globals.scss file and compile (see Project Compilation)

###Demo Files
All working demos can be found in the dist -> demo root. Demo files are all executable html with proper markup for using the specific ui element or component. 
> Demo subfolders use the same explicit naming conventions as the scss files themselves. (i.e. the demo html for the ui > component > form > checkbox.scss file will be in the demo ui > component > form > checkbox.html file). 

###Semantic Classes
Custom classes use a common semantic format to make them easier to understand and implement. A good example of this is how the padding normalizer is marked up. To apply a 5 px padding to the horizontal borders of an element, you would associate a class called padding_5_horizontal. This allows us to avoid using complex compound selectors. Other elements use the same semantic markup.

###Buffers
Buffers relate to margin and padding values of an element. Buffers are display properties placed inside or outside of an html element. Buffers use a basic semantic logic : buffer_value_position. This outputs to margin_20_bottom. To invalidate a buffer on an element, the semantic logic is buffer_null. This outputs as padding_null. To achieve this class semantic, the scss
file is written with omitted class definitions (i.e. .pad{&_null{padding:0;}}.

###Grid System
The grid system used in this bootstrap is a 1-6, 8, 12, 24 column model. Columns can be placed in a containing row model that defines their maximum width, or placed outside of a row  to allow for a more fluid organisation. The grid system is responsive and therefore uses percentage width values instead of fixed pixel formats. Grid classes use the following semantic logic : _size-column-totalColumns. This outputs to _size-1-12.

###Optic Modifiers
Optic modifiers are class selectors that change specific visual aspects attributed to an html element. Following the defined semantic class markup, their format is .optic_value. For example, an opacity 50 value would have the class .alpha_50.

###Overrides
Overrides are global definitions applied to one or many html elements. Overrides are usually used to avoid browser issues and establish global styling guidelines. The _overrides.scss file is also where you can define a site-wide font.

###Modifying Root SCSS Files
You can modify any class or selector in the scss file root. Make sure to create a backup of the original scss file using the namig convention _original-file##backup.scss
>It is recommended to create custom scss files in the collaborate root instead of modifying the existing scss files. You can add your custom scss in the globals.scss file and remove the association to the original file. 

###Required Files
All required files are found in the scss -> base -> required folder. They should always be called at the top of your globals scss file, right after the settings (if any). If this is not the case, variable and mixin definitions may now work properly. 

###Color Palette
A variable based color palette can be found in the scss -> base -> required -> variables -> colors folder. You can add new color codes or select the color palette you wish to include in your project by removing unused color variables from the globals scss file. 

###Source Directory
This folder contains required third party scripts, styles or elements. When extending the bootstrap, add all required third party elements to this folder and reference them in the demo file you create. 
>When using third party elements in your project, it is recommended to copy them from the src folder to a working asset folder in your project root.

###Author
```sh
David Maser david.maser@altitude-sports.com
```
###Third Party Resources
```sh
Please consult the package.json file for a list of third party resources and components used in this project.
```
