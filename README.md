# Wrapbin

EXPERIMENTAL EARLY WIP.

Wrap executable files in to customizable scripts

## Usage

```
wrapbin update $PATH
```

Wrapbin gets every executable file in $PATH and make corresponding scripts at `/usr/bin/wrapbin`.

## Configuration

### /etc/wrapbin/conf

Basic configurations

### /etc/wrapbin/rules.d

In these files, each line specifies which template should be used for the executable file path.

```
/usr/bin/someprogram python_is_python2
```

### /etc/wrapbin/templates.d

Each file is a script template.

```
#!/bin/bash

# Example rule: python_is_python2
/usr/bin/python2 $wPROG "$@"
```