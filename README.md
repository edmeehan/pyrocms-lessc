#PyroCMS Less Compiler Plugin
=============================
###Plugin - Easy part
Edward Meehan @ Wetumka Interactive LLC

###PHP Compiler - The guy that did the hard part
https://github.com/leafo/lessphp
http://leafo.net

#How to use

I set up a conditional in my views/partials/metadata.html - this way I use the compiled files on production and also can test in my staging environment.
```
{{ if global:environment == 'development' }}
<!-- DEVELOPMENT FILES -->
{{ less:compile file="build.less" output="style.css" }}
{{ else }}
<!-- PRODUCTION FILES -->
<link rel="stylesheet" href="/{{theme:path}}/css/style.css" />
{{ endif }}
```