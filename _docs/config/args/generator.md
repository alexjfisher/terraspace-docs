---
title: Arg Generator
nav_text: Generator
categories: args
order: 9
---

To help you get started quickly, you can generate starter arg code. Here are some examples:

## Cheatsheet

    terraspace new arg --type project
    terraspace new arg demo --type stack

## Project

    $ terraspace new arg --type project
          create  config/args
          create  config/args/terraform.rb

Produces:

config/hooks/terraform.rb

```ruby
command("apply",
  args: ["-lock-timeout=22m"],
)
```

## Stack

    $ terraspace new arg demo --type stack
          create  app/stacks/demo/config/args
          create  app/stacks/demo/config/args/terraform.rb

## Module

    $ terraspace new arg example --type module
          create  app/modules/example/config/args
          create  app/modules/example/config/args/terraform.rb
