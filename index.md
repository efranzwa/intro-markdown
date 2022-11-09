# Content for an H1 Header
## Content for an H2 Header
### Content for an H3 Header
#### Content for an H4 Header
##### Content for an H5 Header
###### Content for an H6 Header
![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

#### some bash code

```bash
#!/usr/bin/env bash

bindir=
logdir=

## Command parsing ################################################################################
cmd="${1}"; shift

## Argument and option parsing ####################################################################
while (( "$#" )); do
  case "${1}" in
    --channel=*) channel=${1/--channel=/''}; shift ;;
    --quality=*) quality=${1/--quality=/''}; shift ;;
    -c*) channel=${2}; shift; shift ;;
    -q*) quality=${2}; shift; shift ;;
    *)
      case "${cmd}" in
        listen|play) test -n "${1}" && test -z "${channel}" && channel=${1} ;;
      esac
      shift
    ;;
  esac
done
```
