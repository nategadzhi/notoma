---
layout: default
nav_order: 2
title: Using the Command Line Tool
---

<!--
THIS FILE IS AUTOGENERATED, DON'T EDIT.
File to edit instead: notebooks/using-the-cli.ipynb
-->

# Using the Command Line Tool

Getting started with the CLI tool. This notebook also moonlights as an integration test, as actually runs the example commands.
<div class="codecell" markdown="1">
<div class="input_area" markdown="1">


```python
!notoma --help
```

</div>
<div class="output_area" markdown="1">

    Usage: notoma [OPTIONS] COMMAND [ARGS]...
    
      Build your staticg gen blog with Notion. Notoma converts Notion database
      of blog posts into a directory of .md files.
    
    Options:
      --help  Show this message and exit.
    
    Commands:
      convert  Convert Notion Blog to Markdown files.
      new      Create a new Notion Blog
      version  Print Notoma version.
      watch    Watch for updates in the Notion Blog and update the Markdown...


</div>

</div>

## Convert

Converts the Notion blog database to a bunch of markdown files in a specified directory.
<div class="codecell" markdown="1">
<div class="input_area" markdown="1">


```python
!notoma convert --help
```

</div>
<div class="output_area" markdown="1">

    Usage: notoma convert [OPTIONS]
    
      Convert Notion Blog to Markdown files.
    
    Options:
      -f, --from TEXT      Notion blog URL
      -d, --dest PATH      Directory to put posts into.  [required]
      --drafts PATH        Directory for draft posts. Drafts won't be imported if
                           this is left blank.
    
      -t, --token_v2 TEXT  Notion auth token from the cookie.
      --verbose            Verbose output.
      --debug              Enable debug output.
      --help               Show this message and exit.


</div>

</div>

Despite `--from` and `--token_v2` options are not requreired in the CI help output, you must provide them in the command line, or in the `.env` config file.

If you try running `notoma convert` without providing them, notoma will fail with an error message asking for these options. 

## Watch

Not available yet.

## Create

Not available yet.
