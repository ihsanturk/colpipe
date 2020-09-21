# `colpipe`
Pipe a specific column to a command that takes its inputs from standart intput.

## Example
Let's say I have a command called `timestamp2date` and I want to replace the content of just the second field of "mydata.txt" with their date values instead of timestamps and output the result to "human-readable-dates.txt".
```sh
cat mydata.txt | colpipe -f2 -c 'timestamp2date' > human-readable-dates.txt
```

cat mydata.txt
```txt
438	1600637364	some other field of my data
439	1600638829	iamanerdiamanerdiamiamanerdiamanerd
440	1600684876	cryptictextguysyeah
441	1600685341	iamwritingthisat3pmokayiamnotafreak
442	1600701927	youareanawesomepersonthatdontmissessmalldetailsrightimeanyouareactuallyreadingthis
```

cat human-readable-dates.txt
```txt
438	2020-09-20T21:29:24UTC	some other field of my data
439	2020-09-20T21:53:49UTC	iamanerdiamanerdiamiamanerdiamanerd
440	2020-09-21T10:41:16UTC	cryptictextfortheexampleguysyeah
441	2020-09-21T10:49:01UTC	iamwritingthisat3pmokayiamnotafreak
442	2020-09-21T15:25:27UTC	youareanawesomepersonthatdontmissessmalldetailsrightimeanyouareactuallyreadingthis
```
