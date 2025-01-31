# File hashes for all R packages

2020-11-21 

This is a set of csv files that contain filehashes for all the packages
found on the archive of CRAN and currently active. 

My thinking is that you should be able to verify that you have the exact same 
tar.gz files by comparing the hash you get of that file with this list.

For example:

```
A3_0.9.1,93b9bbb89f61a130eaf811f7d64e3223693ab6a2b09696d0f36325df7c7ce11c
A3_0.9.2,345c0e4105471ef8a38c2a54cc668dd3d57889686fb4984c9244c17b1045f87a
``` 

If you download the source file for A3 version 0.9.1, and calculate the
sha256 hash of the file it should match the one I supplied.

What are these:

'.csv' files with a packagename_version as 'key' and hash type as 'sha[1|256|512]'

* sha1
* sha256
* sha512 

I also clearsigned the files, `gpg --verify rpgks_sha1.csv.asc` should
give you a signature with my email adress and a key: AD0C7319C25950CDED1DCDE979A514B1EE3CA5DA
. 



## Possible issues
I will try to update these hashes over time, but this should include all
packages currently on CRAN and in the CRAN archives. 

I calculated all these hashes as a side effect of a different project. And so 
I do not have a robust structure in place to rerun the steps.

I downloaded all these packages (tar.gz) from cloud.r-project.org 
a cloud mirror of the official repository. So if there is an evil person
in the middle impostering official CRAN, the mirror could be poisened.
I have no qualifications, but my naive thinking is that that would be
quite difficult. 

I make no guarantees about the qualities of the package. CRAN does a 
manual review process that is quite thorough, I did not check any package.

Another possibility is that my downloads were poisened between cloud.r-project.org and my computer. 
That I also deem quite difficult. I used an up to date computer (ubuntu 20.04) and 
all downloads were over encrypted tcp connection (https connection).

Overall I think we are pretty good here. But please please remember I am an amateur!

