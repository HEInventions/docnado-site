 title:      Automated Testing
 desc:       How to (almost) effortlessly test your documentation before deployment.
 date:       2018/10/16
 version:    1.0.0
 template:   document
 nav:        Getting Started>Automated Testing 
 percent:    100
 authors:    enq@heinventions.com

One powerful feature of Docserve is it's inbuilt ability to static check your documentation for broken links, and for those unused assets that are just taking up space.

These are easily invoked from a command line interface, just change your current working directory to the root of your docnado project and we're ready to get started.

```bash
$ cd ~/my_project
$ ls
docs  logo.png  style
```
# Finding Unused Assets
Unused assets (aka orphan files) are files in a project that are not linked to or referenced by any other part of a project. Perhaps you have updated your project over time and they are no longer needed, reminents of an earlier version now just taking up space, or perhaps (even worse) they are important parts of your documentation that you've forgotten to include!

Luckily docnado has a handy tool for finding them.

```bash
docnado --find-orphans
3 Unused assets (orphans):
	/home/username/my_project/docs/this_page_is_not_used.md
	/home/username/my_project/docs/demo/assets/this_is_and_unused_picture.jpeg
	/home/username/my_project/docs/demo/assets/this_pdf_is_not_linked_to.pdf
```

# Finding Broken Links
What happens when the opposite happens, when you link to an asset or web page that doesn't exist? For example you could link to some external webpage that has been moved moved or internal documentation that has been updated, or you could have simply mistyped a web address! That's where our broken link finding tool is here to help.

```bash
$ docnado --find-broken-links
/home/user/my_project/docs/home.md
	/home/user/my_project/docs/assets/this_does_not_exist.pdf
/home/user/my_priject/docs/demo/text.md
	https://github.com/boltdb/raw/blob/master/READM.md
```
