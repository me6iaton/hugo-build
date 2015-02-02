# Wercker Step Hugo Build

runs [Hugo](http://gohugo.io) bin file on the source code in order to generate the static site. This can then automatically be deployed using other steps.

# Parameters

## bin (optional/recommended)

Path for binary file hugo from WERCKER_SOURCE_DIR, default: bin/hugo-linux

## theme (optional)

Specifies the theme to be used for the generation of the site. When this isn't defined no theme will be used.

## flags (optional)

Apart from the theme, other flags can be provided as a single string. These flags will be provided exactly as set.

# Example wercker.yml

```yml
box: wercker/default
build:
  steps:
    - arjen/hugo-build:
        bin: bin/hugo-linux-x64
        theme: hyde
        flags: --disableSitemap=true
```
