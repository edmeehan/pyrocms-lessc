#PyroCMS Less Compiler Plugin
=============================

Plugin by - Edward Meehan @ Wetumka Interactive LLC

PHP Less Compiler - github.com/leafo/lessphp

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