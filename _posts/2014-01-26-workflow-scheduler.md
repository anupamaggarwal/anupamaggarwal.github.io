---
layout: post
title: AgentSmith
category: programming
time: "3:17"
---


Workflow-scheduler

![agentsmith](http://bgowiki.terrywri.st/images/b/b3/Agent_Smith.jpg)

*Smith began as an Agent, programmed by Anupam to keep order within the system by terminating human simulacra which would bring instability to the simulated workflow stream of the application, as well as any rogue programs like cron that no longer serve a purpose to software collective
To this end, Smith possesses the ability to take control over the simulated body of any functions wired into the workflow*

AgentSmith is a workflow scheduler which can be used to stitch together a workflow (set of tasks) over a set of machines.



```
Look at workflow.py to get an idea of how to use agentsmith
```



####TODOS

1. Log rotate execution by day



####CAPABILITIES

v.01 < alpha release >
1. Basic monitoring and alerting (define your monitoring commands, send emails in case of failures)
2. Schedule a job at periodic time intervals on arbitary hosts
3. Execute the said jobs and alert if there are errors
4. Simple web interface for process monitoring (Each process governs running of a workflow)
5. Schedule a job in background (remotely or local)
6. Trigger dependent jobs based on job completion etc


<blockquote>Scratchpad</blockquote>

Http request to add/ delete a job to scheduler Print status of a long running jobs dependent on task monitored via email prefixing with some specific names to avoid nameclashes with python dependenvy information in fabfile scheduling information in apscheduler file tasks return a valid code when they execute decorated with background or foreground decorated with email on failure option of firing individual task ption of firing at specific time waitondecorators (done file) state of jobs in a shelve store (custom store) decorated with background or foreground decorated with email on failure option of firing individual task option of firing at specific time @parallel/serialize @background @email @dependent() offline/background execution email_on_fail email logs on failure in the fabric file background dependent(copy_task,memcache_task) foreground template background with agent smith picture shutdown take care of tasks config relating to coalesing etc email files kick jobs script takes input and a done file

####SOFTWARE STACK AND DEPENDENCIES

* Tornado as the webserver
* Fabric for remote execution and monitoring
* Python Versions 2.6+
* ApScheduler to execute jobs

<blockquote>
INSPIRATION
</blockquote>

Flower / celery task monitoring
