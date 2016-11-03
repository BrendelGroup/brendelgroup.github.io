---
layout: post
title: "Why design workflows for computational genomics?"
date: 2016-11-02T22:37:02 -04:00
---

The other day I was asked about the difference between _pipelines_ and
_workflows_.
Good question!
On first impulse, my answer was that _pipelines_ are what plumbers deal with,
whereas we are designing _workflows_.
This was a disingenuous answer, however.
After all, we are constantly using Linux _pipe_ commands to string together
various tasks on the command _line_.
A more apt answer would have been that _workflows_ are generalizations of
pipelines, which allow for more complex than linear flows of input to output.
A typical workflow may involve several branches that can be executed
independently and in parallel.
In practice, we use combinations of
[Linux _bash_](http://www.tldp.org/LDP/abs/html/) scripts,
[R](https://www.r-project.org/) scripts, and
[GNU make](https://www.gnu.org/software/make/) files to execute simple,
compound, and complex workflows, using whatever tools are most appropriate to
the task at hand.

Why should we or anyone else design workflows for computational genomics?
The first argument for workflows centers on _reproducibility_.
In fact, much of our current focus on workflows stems from a recurrent problem:
ask a student (or anyone) how exactly they produced a particular result, and
after a lot of hesitation, head-scratching, and time spent searching, more
often than not no satisfactory answer will be given.
Here, "satisfactory" means to me that I can reproduce all the computational
steps that led to the reported result, simply taking the same input and
following the same steps.
Of course this is a very reasonable demand (barring applications that involve
random seeds, in which case we should not expect to produce exactly the same
results).
But in practice we should modify the request to ask for "easy reproducibility".
In other words, I and any other reviewer should be able the reproduce the
results with minimal effort (although our computers may have to do a bit, or
maybe quite a bit of work!).
Thus, when we talk about _workflows_ we actually imply complete computational
prescriptions that take data and parameter input and produce desired output -
which in computational genomics might be hundreds of gigabytes of files on
disk.

A second argument for workflows relates to _scalability_.
Rarely do we run a computational experiment just once.
Much more typical is that there is a lot of trial and error until we get
everything conceptually right.
Then we explore different parameter settings for the various programs.
Lastly, once we got one data set analyzed, there is likely another date set
waiting to be looked at.
Not to forget that if we find the workflow useful, then likely others will, too.
What nicer way to share but to given them access to the whole set of recipes,
ready to run on their own computers with a few keystrokes?

(Volker Brendel, Indiana University)
