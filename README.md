# git-tricks
Git tips advanced tricks

## Useful commands
git checkout -b <new_branch>

git log -p
(print diff)

git log --stat
(print stats e.g lines added or number of files added and removed)

git log --oneline
git log --oneline --graph

git log --oneline --graph --decorate
(Many times it’s useful to know which branch or tag each commit is associated with)

git shortlog
(Special version of `git log` groups each contributor commits)

## Filtering
### By Number
git log -<number>
(Picks recent commits)

### By Date
git log --after="2014-7-1"
git log --before="2014-7-1" 
git log --after="yesterday"
You can also pass in relative references like "1 week ago" and "yesterday"

### By Author
git log --author="John"

### By Message
To filter commits by their commit message, use the --grep flag. This works just like the --author flag discussed above, but it matches against the commit message instead of the author.

git log --grep="JRA-224:"

### By File
Many times, you’re only interested in changes that happened to a particular file. To show the history related to a file, all you have to do is pass in the file path. For example, the following returns all commits that affected either the foo.py or the bar.py file:

git log -- foo.py bar.py
The -- parameter is used to tell git log that subsequent arguments are file paths and not branch names. If there’s no chance of mixing it up with a branch, you can omit the --.




