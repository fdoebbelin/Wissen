This blog covers how to automate daily Robocopy jobs using Task Scheduler.

Again, the syntax I choose is:

***robocopy*** ***\\\sourceserver\\ShareName*** ***D:\\Shares\\ShareName /e /b /copyall /PURGE /r:5 /w:5 /MT:64 /log+:D:\\Shares\\log\_ShareName \_%date:~-10,2%”-“%date:~7,2%”-“%date:~-4,4%.txt /v***

Recall I recommend removing the /tee parameter when not caring to see the output displayed to the screen, as you would not see it in this scheduled task.

Additionally, I recommend testing out your exact line of code before creating the batch file. Once you have finalized it, create a new text file, rename it to have a .bat file extension, and then edit it, putting in one Robocopy line with parameters you will use.

![](task1-1024x137_91769dbb3685438780ba6976acbedcce.png)

I typically try to create one batch file per share I’m copying instead of putting multiple Robocopy jobs in one batch file. This generally is for troubleshooting purposes, but if you wanted, you could create just one batch file for various Robocopy jobs.

Launch Task Scheduler your favorite way by searching for it in the Control Panel:

![Robocopy Using Task Scheduler](task2_7e3916af5185495e91ef08a7d80f872d.png)

Or by simply launching it from the Tools menu in Server Manager.

Or by searching for it from the Start menu:

![](task3_5435efb5951d4507bf0bb6d2058cdc34.png)

Once launched, select the Task Scheduler Library to view current scheduled tasks. Right click it and select “Create Basic Task…”

![Robocopy Using Task Scheduler](task4_6eb0d67aff7e4b2c96cdfdd87fc1ef4a.png)
A wizard will launch. Enter a useful name and a description (optional) of the task.

![](task5_bd8416714a974d01983227cbdb6094e4.png)

Choose the frequency of the task. I prefer to run these daily.

![Robocopy Using Task Scheduler](_resources/task6_01fb9046f1094c0cad2927540061bb54.png)

Pick the start date and daily time the task will run and leave it to recur every day.

![](_resources/task7_b1446124c3e14f6ea2bfdfdcab961154.png)

Leave the action to “Start a program.”

![](_resources/task8_65d3a820d1214a7fa7ea684faebe35fb.png)

Browse for or manually type in path to the batch file. No additional arguments are required.

![Robocopy Using Task Scheduler](_resources/task9_b1ed4721e4084cb9a3600407f9b75b58.png)

Review the settings configured. Check the box to “Open the Properties dialog for this task when I click Finish.”

![](_resources/task10_a0219a5f95504c6e95f5fd742a8e9abe.png)

Select the option button to “Run whether user is logged on or not” and the check box for “Run with highest privileges.” It also may be necessary to change the user of the job running if you don’t want the task to run with the previous user account.

![](_resources/task14_916c43be5bbf4809a310ee2df986692f.png)

I also usually have the task stop if it has been running longer than one day. To do this, click on the Settings tab, then change the default three days to 1 day. This is where you would have done your homework ahead of time to see how many files and folder and their size and estimate how long it will take to copy to the new server. If unsure, just leave it the default three days and check the logs generated afterward to see if it completed or if it needs a longer run window.

![Robocopy Using Task Scheduler](_resources/task11_3ed84225a8924c05a78c90369f696328.png)

Clicking OK will prompt for the user account information that will be running the task. This saves the credentials in Task Manager. Be sure to enter the domain in the username field along with the username.

![](_resources/task12_455b1b18545241f4acee5ce554a0609d.png)

Create additional tasks by using the same method as above or slightly more quickly by exporting the task already created to an XML file, then modifying a few things in the XML file (Description, URI, StartBoundary, and Command). When importing, verify the settings are the same as previously configured as you may lose some settings during the import.

The benefit to creating Scheduled Tasks to run these jobs are:

- It will run by itself.
- You don’t need to log into the server to do it.
- For the most part, running it daily will equate to a smaller delta on the actual cutover day.
- You can run it manually very quickly instead of finding the correct syntax all over again.

**Be sure on the actual cutover day to disable and/or delete the task! Failure to do so will mean that new active data on the active share will be deleted because it doesn’t exist on the old share!**

For the actual cutover, change the source server’s shares to Read Only to prohibit users from changing file and run the task one last time (right-click the task and click Run).

![](_resources/task13_8c6612c47223495b966490cf6a948852.png)

Be sure to review the logs outputted to see if there are any errors due to syntax or locks on the files. Putting the share in Read Only or a server reboot should do the trick if necessary if there is a lock.