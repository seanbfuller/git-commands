# Git Commands

## Yearly counts

Get a count of commits for this year
```
git rev-list --count HEAD --since="Jan 1 2016" --before="Dec 31 2016"
```

Get a count files and lines changed
```
git log --shortstat --since="Jan 1 2016" --before="Dec 31 2016" | grep "files changed" | awk '{files+=$1; inserted+=$4; deleted+=$6} END {print "files changed:", files, "lines inserted:", inserted, "lines deleted:", deleted}'
```