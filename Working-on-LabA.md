Walking into the lab I obviously thought it would be easy. That would be my first surprise of the day!

Logically speaking the lab was actually fairly easy, instructions seemed easy to follow. It was just basic installation and configuration of a Docker container to run executable files provided through a sandbox server. Docker stopped being scary a while ago, so I was pretty confident in my abilities... and that's where I was wrong.

Apparently Docker on Fedora 29 just doesn't work the way the assignment intended and was throwing very weird errors when trying to log in with any other user but root. Not only that but even after I logged in with the root user and "su" my way into the new user I created I just couldn't pull the necessary executables.

Banging my head deep into the wall and creating new Docker containers left and right, I decided that maybe, just maybe the Docker in the assignment was specifically created for Ubuntu, since the documentation seemed Ubuntu-oriented. Sure enough, after creating a Virtual Machine running Ubuntu Server 18.04 LTS everything started working.

Logging in to the Docker container was no longer an issue, executables were downloading fine. Despite all prior experiences I began feeling... hope

Now, almost 4 hours later I am still unsure what happened, what was the root cause for these issues, but I am way too happy to troubleshoot it any further. Now I'm only hopeful it will not break again next week...
