Seven One Architecture for Sass

In this architecture we keep 7 folders in sass main folder and a main.sass .
Fist folder is "base" folder, in it we have files as:
1. _base.scss : 
-> For real low level basics. such as presets, and style for html and body. 
-> This file must be a partial so that later we can import it in main.sass . 
-> Partial files always start with underscore. so we name this file as _base.scss (scss is one of syntax of sass)
-> To import this file in main.scss we just use:
@import 'base/base';

first base is directory name and another base is partial name. Note we not include underscore, as 
sass compiler automatically understand that it is partial and can be included without underscore.

2. _animations.scss
3. _typography.scss
4. _utilities.scss

Next folder is "abstracts", in it we keep files that not going to output any css like variables, mixins etc.
so files in it are as:
1. _variables.scss
2. _mixins.scss
3. _functions.scss

Next folder is "components", in it we keep files that contribute to reusable block that can be used anywhere in page.
Next folder is "layout", in it we have sass for header, footer.
Next folder is "pages", for specific pages, like for home page we can have _home.scss
Next 2 folders are themes and vendor. In vendor folder we can keep 3rd party files and themes we can 
put scss rules for different themes. We can omit these or any folder application don't require it.

files in components, layout, themes, pages, and vendor are not standard files. They are just added to 
commit code on git.

main.scss is only for import file not for writing any scss rule.