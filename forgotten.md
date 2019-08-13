# shit that i have forgotten more often than not

`grep -rnw '/path/to/somewhere/' -e 'pattern'`
-r recursive
-n line number
-w whole word
-l lowercase
`grep --include=\*.{c,h} -rnw '/path/to/somewhere/' -e "pattern"`
`grep --exclude=*.o -rnw '/path/to/somewhere/' -e "pattern"`
`grep --exclude-dir={dir1,dir2,*.dst} -rnw '/path/to/somewhere/' -e "pattern"`

tar czfv test.tar.gz test/
# If you want bzip files, use "j" instead of "z".
# Again, if you want bzip files, use "j" instead of "z".
tar cvf ~/app.tar --exclude .git --exclude "*.log" ./
