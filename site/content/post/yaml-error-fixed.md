---
title: 'YAML error fixed '
date: 2018-01-11T23:34:52.122Z
description: >-
  Indentation is key with YAML. Make a mistake and your code will not compile,
  be counting when hitting the spacebar
---
Each time you indent in YAML that is the value for the parent key. If your parent key already has a value you can not indent.

### Wrong:
Code (Text):

- _key1:_
    - _key2: ***value***_
        - _key3: value_
___
### Right:
Code (Text):

   - _key1:_
       - _key2:_
           - _key3: value_
     
#### key3 is the value for key2.
BillyGalbreath, *Jul 5, 2015*

>Error: Error building site: Errors reading pages: Error: failed to parse page metadata for "_index.md": yaml: line 5: mapping values are not allowed in this context for _index.md
>
