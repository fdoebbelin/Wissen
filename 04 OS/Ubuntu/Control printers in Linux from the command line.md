Use this in-depth tutorial to master the troubleshooting and administration of Linux printers.

Everyone knows that Linux makes a great Web server. Some network administrators even use it in conjunction with Samba to create file servers that Windows workstations can access as easily as Windows NT/2000 file servers. However, if you want to use your Linux server as a print server, you can do that too. The most effective way, although not always the easiest, is using Linux print utilities.

* * *

Author's Note  
This article is based on command lines available in RedHat Linux 9.0, the latest release available. Each flavor of UNIX has slightly different command lines, and some UNIX flavors are not yet using CUPS, so the commands can be very different. A good idea is to take a look at the main page for the various command lines to examine and choose the proper options. I will point out some of the differences in commands throughout the article.

* * *

Who needs a GUI?  
Keep in mind that most flavors of UNIX have a GUI printer administration tool. Several different environments are packaged with Redhat 9.0 Linux. This article will give you the basics on how printers work, how to configure them, and how to maintain them with command line options.

Many people prefer GUI interfaces when working with operating systems they're not completely familiar with because they're easier to use. Once you have a good understanding of the system, you may find that command line utilities give you more granular control over the printing environment while also allowing you to make modifications more rapidly. Rather than click, wait, click, wait, click, wait, you can just type the commands in a terminal window, press \[Enter\], and be done.

CUPS  
Many flavors of Linux have adopted the new printing standard, CUPS (Common UNIX Printer System). This is the first update to the UNIX printing world in many years. It allows items such as:

*   Native support for IPP, Internet Printing Protocol
*   Native support for Windows printers
*   The ability to browse network printers
*   Support for PPD, PostScript Printer Definitions

Prior versions of UNIX print services were based mainly on line printers, those old huge impact printers that only printed text on green bar paper. CUPS allows a lot of functionality and gives support for many more printers. It also allows all of the graphical capabilities that were lacking.

Linux print commands  
Linux has several different print commands that you can use from a terminal window. Most of the commands can be used by both the logged on user id as well as by root. Others work only from root. The following is a list of the utilities that allow you to administer and control the printing system that you can use when logged in as either user or root:

*   /usr/bin/lp - Used to submit print jobs
*   /usr/bin/lp.cups - Used to submit print jobs
*   /usr/bin/lpoptions - Gets and sets printer options for a single user when run by a user or for the system when used by root
*   /usr/bin/lppasswd - Changes printing passwords for an individual user or adds, deletes, and changes printer users and passwords when run by root
*   /usr/bin/lpq - Shows the status of a printer queue
*   /usr/bin/lpq.cups - Shows the status of a printer queue
*   /usr/bin/lpr - Used to submit print jobs
*   /usr/bin/lpr.cups - Used to submit print jobs, forcing use of CUPS
*   /usr/bin/lprm - Used to remove print jobs from a queue
*   /usr/bin/lprm.cups - Used to remove print jobs from a queue
*   /usr/bin/lpstat - Gives status of the CUPS system, such as queue lengths and printers
*   /usr/bin/lpstat.cups - Gives status of the CUPS system, such as queue lengths and printers
*   /usr/bin/cancel - Cancels a print job
*   /usr/bin/enable - Enables a print queue or class of printers, requires a management password
*   /usr/bin/disable - Disables a print queue or class of printers, requires a management password
*   /usr/sbin/lpadmin - Manages printers and classes, requires a management password
*   /usr/sbin/lpc - A compatibility program for Berkley style printers, limited to queue status in CUPS
*   /usr/sbin/lpc.cups - A compatibility program for Berkley style printers, limited to queue status in CUPS
*   /usr/sbin/lpdomatic - A filter script provided to be used in setting up printers
*   /usr/sbin/lpinfo - Shows available printer devices and drivers on the system
*   /usr/sbin/lpmove - Moves the jobs destined for a queue to another queue

These commands only work when you're logged in as root, either when you log in or after switching to root using the _su_ command:

*   /usr/bin/lprsetup.sh - A shell script provided to help set up ghostscript printers
*   /usr/sbin/accept - Causes the print queue to accept requests
*   /usr/sbin/reject - Causes the print queue to reject requests

You may notice that some commands have the .cups extension, while others don't. If you're coming from the Windows world, this may be confusing. Normally, executables only end in .EXE or .COM. Here, the commands with .cups in their name are the actual executables. Most of the non-cups commands are symbolic links, which point back to the executables with the .cups extension. For example, if you do a long listing, _ls –l_, on /usr/bin/lp you would find:  
  
\# ls -l /usr/bin/lp  
lrwxrwxrwx    1 root    root           26 Jun 11 12:11 /usr/bin/lp -> /etc/alternatives/print-lp

The executable for /usr/bin/lp is a symbolic link to /etc/alternatives/print-lp. If you do a long listing, _ls –l_, on the symbolic link you will find it is also a symbolic link:  
  
\# ls -l /etc/alternatives/print-lp  
lrwxrwxrwx    1 root     root           16 Jun 11 12:11 /etc/alternatives/print-lp -> /usr/bin/lp.cups

So you can see /usr/bin/lp is actually using /usr/bin/lp.cups.

This may seem somewhat confusing at first, but what these links assure is compatibility for those administrators who are used to BSD, or Berkley, equivalents, or to System V equivalents of commands. Many times they don't have the same options, but it does provide at least the same command structure.

Setting up a printer  
Now that you know the basics of the commands, let's consider the following scenario. You have a Hewlett-Packard LaserJet V attached to your Linux box using the first parallel port. The first step in adding the printer is to be sure you are root, so either log in as root or use the _su -_ command to become root. This ensures all the printer commands can be executed and will be found in your path.

lpstat  
In order to add the printer, you must first check what printers are already available on the system so as not to assign the new printer to a port that is already in use. To check the system for printers and their status, use the lpstat command. Specifically, in order to see the status for all of the printers on the system, as well as the scheduler and all jobs, use:  
  
\# lpstat -t

If your system currently does not have any printers installed, the output should look something like:  
scheduler is running  
no system default destination

Like most command line utilities, lpstat has several switches that allow you finer control. Some of these other switches for the lpstat command include:

*   -a \[_printer name(s)_\] \- Report the acceptance status of the printers
*   -c \[_class name(s)\]_ \- Report the printers in the class(s)
*   -l - Long listing of printers, classes, and jobs
*   -r - Tells if the scheduler is running
*   -h &lt;server name&gt; - Connect to the CUPS &lt;server name&gt;
*   -s - Summary of all printers, classes, and associated devices

lpadmin  
Once you have confirmed that the scheduler is running and the device you want to use is free, the next step is to add the printer using the lpadmin command. The lpadmin command allows you to configure all the necessary items to add the printer to the system. To add the laser printer specified in the example above, use the command:  
  
#  lpadmin -p laserjetV  -m laserjet.ppd -v parallel -D "HP LaserJet V" -L "Office 502"

The options used here include:

*   -p laserjetV - the name of the new printer
*   -m laserjet.ppd - the specification of the Postscript Printer Description file so CUPS knows how to speak to the printer
*   -v parallel - specifies the device to be used for the printer
*   -D "HP LaserJet V" - a textual description of the printer
*   -L "Office 502" - a textual description of the location of the printer

If the command is successful, the return from the command will be nothing. If there is an error, the type of error will be reported.

Other options for the lpadmin command include:

*   -c &lt;class name&gt; - The class to put the new printer in. If it does not exist, the class will be created.
*   -o job-page-limit=value - Set the option to limit the number of pages submitted in any one job.
*   -o job-k-limit=value - Set the option to limit the kilobyte size submitted in any one job.
*   -E - Automatically enables the printer and causes the printer to accept requests. This will be explained later.

To check the completion of the command, you can run the _lpstat -t_ command again. You should see output similar to:  
  
scheduler is running  
system default destination: laserjetV  
device for laserjetV: parallel  
laserjetV not accepting requests since Jan 01 00:00 –  
  
printer laserjetV disabled since Jan 01 00:00 –

Notice that the default destination has been set to the printer that was added. The reason? It is the only printer on the system. Also notice the printer is both disabled and not accepting requests. This is the automatic setting for the printer, so the administrator can do any other maintenance that is necessary before allowing users access to the printer. As mentioned above, the -E option can be used to enable and set the printer to accept requests. Only use this option if you are sure the printer is ready to be used.

enable  
Once the configuration and set up is complete, use the enable command to enable the printer:  
  
\# enable laserjetV

When enable completes, run another lpstat command:  
  
\# lpstat –a –p laserjetV

-a shows the acceptance status and -p laserjetV displays the printer you're interested in. The output should be:  
  
laserjetV not accepting requests since Jan 01 00:00 -  
printer laserjetV is idle. enabled since Jan 01 00:00

accept  
At this point, the printer is enabled, but still not accepting requests. In order to have the printer accept requests, run the command:  
  
\# accept  laserjetV

Using another lpstat -a will show the following:  
  
laserjetV accepting requests since Jan 01 00:00

Note the accept command is slightly different from the other commands used so far. It does not use the -p option; instead, it just requires the printer name.

The difference between enabled and accepting requests should be noted here. When a printer is accepting requests, a user is able to submit a print job to the printer, even if it is not enabled. This allows short maintenance to be completed on the printer while still allowing jobs to be submitted. If the printer is not accepting requests, a user submitting a job will receive an error. In other words, the administrator can disable a printer to change paper or to change toner, but the scheduler will still accept the request.

disable  
If you would like to disable a printer, it is possible to use the command:  
  
\# disable laserjetV

Other options for the disable command include:

*   -c - Delete all jobs in the queue for the destination specified
*   -r - Provide text as a reason for the printer being disabled. It will show up in an lpstat command to notify users why the printer is down.

lpr  
Now the printer is ready to be used by any application or by the users. An example of how to use the printer from the command line is:  
  
\# lpr –P laserjetV –#2 /home/user1/file1

where -P laserjetV prints to the laserjetV printer, -#2 prints two copies, and /home/user/file1 is the name of the file to be printed.

It should be noted that many of the standard lpr options, such as -c and -d, are not available when using cups as the server. Remember that the actual executable is the lpr.cups, which will not accept the options that are not available for CUPS.

Other options for the lpr command include:

*   -C &lt;job name&gt; - Specifies the name of the job to be shown in the queue
*   -l - Specifies that the file is formatted for the default configuration of the printer and that there is no need to use a filter

cancel  
One of the things a user might want to do is remove a job from the print queue. There are two options for the user to choose. The first is the command:  
  
\# cancel &lt;print request id&gt;

The print request id can be found from an lpstat command. The second choice for deleting a print job is:  
  
\# lprm –P laserjetV &lt;print request id(s)&gt;

where -P laserjetV removes the request from the printer laserjetV and &lt;print request id(s)&gt; indicates which requests should be removed.

If you want to cancel all requests for a destination, substitute a - for the print request id. If no destination is specified, the currently printing request will be deleted from the default destination.

All that and more  
There are many other commands that you can use to configure and manipulate printers on a Linux system running CUPS. Some of them are in the list of commands above, even though I didn't use them in this example. Many administrators and users will choose to use one of the GUIs available to work with printers on your system. The abilities added by using CUPS over the older spooler systems, such as Internet Printing Protocol, make the management much easier and allow UNIX systems to use many more printers than were available before.

It is important to note that one of the other features available using CUPS is greatly increased security for printing. Most of the commands discussed have an option to make a secure connection to the CUPS server so that packets cannot be intercepted. For more information about CUPS, see the Daily Drill Down ["CUPS brings a universal standard to Linux printing"](https://www.techrepublic.com/article.jhtml?id=t01520020505mci01.htm).