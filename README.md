# Solutions to Adhoc problems

Q1 # need to iterate over x number of repositories and update them all locally

A1 # find . -type d -print0 | xargs -0 -L1 sh -c 'cd "$0" && pwd && git pull --rebase'

