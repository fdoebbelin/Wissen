![](cf463b7a-4785-483e-948f-719f6061c32c.png)
* `certmgr.mmc`, file->add/remove snap-in, certificates, my user account. 
	* There should be a certificate in `Personal\Certificates` 
	* with a Issued By of `Apple iPhone Device CA`. 
	* Delete it.
* In file explorer, go to `%APPDATA%\Microsoft\Crypto\RSA`. 
	* There should be a folder with a name like `S-1-5-21...` or the like. 
	* Go in there.
* Backup this directory before messing with it.
* Open each file with Notepad, starting with the oldest one. 
	* You're looking for one that has the string `APNSDaemon` in it. 
	* Delete that one.
* Restart the computer and 
	* icloud signin should work now.