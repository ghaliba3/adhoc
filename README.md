# Solutions to adhoc problems i often ask Engineers applying for a role in our team

Q1 # I need to iterate over x number of repositories and update them all locally 

A1 # find . -maxdepth 1 -type d -print0 | xargs -0 -L1 sh -c 'cd "$0" && git pull --rebase'

Q2.1 # If i wanted to output the directories being updated include the base dir and scan the subdirectories of this base dir

A2 # find . -mindepth 1 -maxdepth 1 -type d -print0 | xargs -0 -L1 sh -c 'cd "$0" && pwd && git pull --rebase'
-- ~/ghalib/projects/github/
Already up to date.
Current branch master is up to date.


