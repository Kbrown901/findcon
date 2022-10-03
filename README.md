# findcon
Script bringing ‘find’ ‘cpio’ ‘ebook-convert’ and ‘rm’ together to easily find, convert and copy/remove ebooks and documents recursively through file system starting from your current working directory while keeping file structure.

Prerequisite packages are 'rename' 'find' 'ebook-convert'.
Please install via 'sudo apt install rename find ebook-convert'
I believe 'cpio' is already included with Ubuntu 22.04.1 Server LTS if it's not included in your distro please install that as well.

You will want to double check permissions make sure it is executable, if not run 'sudo chmod a+x '{./your/path}/findcon''
You can then call it from its path (/home/$user/findcon) or move and/or copy it to '/usr/local/bin'.
If you do move/copy it to '/usr/local/bin' you can run it just like any other command. This script works from $cwd so if fo example you have a folder 'ebooks' that is already organized like you want it will keep your file structure but you have to change directory to the top directory that you are wanting to work with. 

Example:
You store your documents/ebooks '/home/$user/Ebooks/' where they are further sorted alphabetically to authors name, ie, '.../Ebooks/'A books'/' '.../Ebook/'B books'/'
In this case you will want to 'cd /home/$user/Ebooks' then run 'findcon'
It will go from '.../Ebooks/' down looking for the specified files to find/copy/convert. All the while preserving file structure.

This is still a work in progress, as such at this time 'rename' is needed, using 'ebook-convert' in this way appends '.$type' to the end of the converted file, ie,
if you are trying to convert '.epub' to '.pdf' in which 'book1.epub' becomes 'book1.epub.pdf' so worked 'rename' in to remove the previous extension so it comes out 'book1.pdf'
