# Git Commands

## Yearly counts

Get a count of commits for this year
```
git rev-list --count --all --since="Jan 1 2017" --before="Dec 31 2017"
```

Get a count files and lines changed
```
git log --shortstat --since="Jan 1 2017" --before="Dec 31 2017" | grep "files changed" | awk '{files+=$1; inserted+=$4; deleted+=$6} END {print "\nfiles changed:", files, "\nlines inserted:", inserted, "\nlines deleted:", deleted}'
```