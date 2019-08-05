---
title: YAML
keywords: cheatsheets
last_updated: August 2, 2019
tags: [cheatsheets encoding]
sidebar: cheatsheets_sidebar
permalink: cs_yaml.html
folder: cheatsheets
---

## YAML syntax

A value:

    value

A value named "foo":

    foo: value

A list:

    - 1
    - 2
    - 'a string'

A list named "bar":

    bar:
      - 1
      - 2
      - 'a string'

Alternate list syntax ("Flow style"):

    bar: [1, 2, 'a string']

A dictionary:

    key1: val1
    key2: val2
    key3: val3

A dictionary named "joe":

    joe:
      key1: val1
      key2: val2
      key3: val3

Dictionary in flow style:

    joe: {key1: val1, key2: val2, key3: val3}

A list of dictionaries:

    children:
        -   name: Jimmy Smith
            age: 15
        -   name: Jenny Smith
            age 12

## Validation

    yamllint foo.yml
    yamllint .
