Developers : Policies documentation
###################################

.. topic:: Overview

    The OMERO development team has put a number of policies and channels
    into place to facilitate interaction.

OME Project Standards
=====================

The purpose of this document is to outline for both current and new members of the OME project how the team works together in order to keep collaborative development moving smoothly. This includes information on everything from daily communication (mailing lists, chat rooms, etc.) to coding practices. Where possible, it points to public resources that anyone interested in OME can also access.


After you’ve read this, you should feel reasonably comfortable with starting to work with and on the project, and at least know how to go about finding out what it is you might not yet know. If you think something’s missing or been left unclear, it’s probably just an oversight. Speak up, and it can be added.


You’re welcome to skip through to sections that interest you, but the intent is that it should be readable from start to finish

Team Collaboration
------------------

For anyone completely new to the project, it’s most important to know how to get plugged in. There’s a fairly extensive amount of communication flying around related to the project, and being able to find and track it may take some time.

Jabber: Instant messaging
~~~~~~~~~~~~~~~~~~~~~~~~~

On a day-to-day level, the team meets in a Jabber chatroom. (See the list of `addresses`_ for the specifics) You’re welcome to join via your own Jabber account, but one will likely be provided to you, in which case that account should be preferred. To get started using Adium:


* File > Join Group Chat (Select your GTalk or Jabber Account in the drop-down menu)
* Use either your GTalk or LifeSci LDAP Account Credentials
* Enter the "Chat Room Name" and "Server"


.. _jabber_screenshot:
.. figure:: images/10000000000001C1000001A8FE75422F.png
   :align:  center


Slightly less frequently, the team meets in teamspeak and/or on skype for having voice discussions. These subgroup, or “minigroup”, meetings are organized as needed, but should provide feedback (tickets, notes, etc) as outlined below. Clients for teamspeak can be downloaded from http://www.teamspeak.com/ and the teamspeak server used by OME is teamspeak.openmicroscopy.org.uk.


.. _teamspeak_screenshot:
.. figure:: images/10000000000001C0000000DAD819C01E.png
   :align:  center


More information is available under


    http://www.openmicroscopy.org/site/community/minutes/conference-calls


As for Skype, being online is not required but it is often beneficial to have it on during the day. Regardless, everyone should have a skype account. Register and download software from http://www.skype.com.
Note: your Skype account name along with all of your contact details should be added to DevContactList on Google Docs. See below.)

Trac: Developer docs
~~~~~~~~~~~~~~~~~~~~

The two major development tools that the OME project runs are Trac and Jenkins.


The Trac server is available under https://trac.openmicroscopy.org.uk/ome and uses your LDAP account for authentication. Trac provides a wiki where we put all the development documentation (as opposed to the official user document under http://openmicroscopy.org).

.. _plone_screenshot:
.. figure:: images/10000000000003EF00000209A486215A.png
   :align: center

Each section of the code base (OMERO, Bio-Formats, the Data Model) has a landing page on the wiki that will direct you to all the "**Getting Started**" documentation that you might need. For example, the page for OMERO is


    http://trac.openmicroscopy.org.uk/ome/wiki/OmeroHome


In addition, Trac is used to record all tickets (i.e. “bugs” or “issues”) as well as hierarchical groups of “tasks” in “requirements” and “stories”. This functionality is provided by a plugin for Trac named “Agilo” (http://agile42.com/) which you may want to read more about. Most importantly it provides a whiteboard where tickets are arranged per story into 3 columns: new, accepted, and closed.


.. _trac_screenshot:
.. figure:: images/10000000000005000000032056C4DB6C.png
   :align:  center


Jenkins: Continuous integration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Our Jenkins server (http://jenkins-ci.org) is available under http://hudson.openmicroscopy.org.uk and also uses LDAP authentication. The name “Hudson” comes from before the Jenkins fork after Sun’s acquisition by Oracle and that’s what the team refers to it as. Hudson provides a mechanism to run arbitrary tasks (“jobs”) on one or more platforms after particular events (time of day, git push, etc.) These jobs build all of the binaries released by the team, and also run automated testing.

.. _jenkins_screenshot:
.. figure:: images/10000000000003EF000002093F36F067.png
   :align:  center

Git and Github: Source code
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Commits take place primarily on github currently. To be aware of what’s really going on, your best option is to become familiar with git, github, and the repositories of all the team members. Information on doing that is available under


    https://trac.openmicroscopy.org.uk/ome/wiki/WorkingWithOmero/UsingGit


.. _github_screenshot:
.. figure:: images/10000000000003EF000002096AD7CA41.png
   :align:  center

Forums and mailing list
~~~~~~~~~~~~~~~~~~~~~~~

Feedback from the OME community happens primarily on 2 public mailing lists (ome-users and ome-devel) that are further described under


    http://www.openmicroscopy.org/site/community/mailing-lists


as well as on the PhpBB forums


    http://openmicroscopy.org/community


an alternative to the mailing lists since some users prefer the forum interface to the mailing list one, and vice versa.


You should add yourself to all three and be aware of and scan all threads on a fairly regular basis. The general rule is that requests from the community will be responded to by the next working day, where to the best of our ability we keep the ‘working days’ and time zones of the community in mind. If you miss any messages or want to review previous discussions see the archive lists available on the “mailing-lists” page:


.. _lists_screenshot:
.. figure:: images/10000000000003EF00000209C6C077E0.png
   :align:  center


Where possible the task of monitoring feedback is spread across the team. For example, Josh and Chris typically monitor the forums and if a message needs to be responded to it will be passed along. Further, all the mailing lists and forums are reviewed for weekly meetings in case any item has been left unnoticed.


Anyone on the team should feel free to speak up to answer questions, but do try to verify the correctness of answers, code samples, etc. before posting.


As much information about our activities and decision processes should be made public as possible. For many items, there is no reason to hide our process, but we don't go out of our way to make them public. For example, internally the team often uses OmniGraffle documents to illustrate concepts, but these are kept privately to prevent any confusion.

Internal Mailing Lists
~~~~~~~~~~~~~~~~~~~~~~

In addition to the two public mailing lists mentioned above, there are also:


* **ome-nitpick@lists.openmicroscopy.org**, used for team-wide, developer communication that isn’t appropriate for the wider OME community such as organizing mini-group meetings, scheduling vacation, etc.; and


* a number of mail-aliases reserved for automated messages from various pieces of development machinery so do not send mail directly to these `addresses`_, instead use ome-nitpick.


Internal Servers
~~~~~~~~~~~~~~~~

There are a number of servers and services inside of the University of Dundee system that are used by the entire team. You may not need access to all of them immediately, but it’s good to know what’s available in case you do.


* **vpn.lifesci.dundee.ac.uk** (LDAP-based) is necessary for securely accessing some of the following resources (e.g. squig, jenkins)


* **squig.openmicroscopy.org** is the shared, team-wide repository for data which can be mounted if you are on VPN or within the UoD system. It contains test data for various file formats.


* The official OME website is run using Plone (https://www.openmicroscopy.org) (LDAP-based)


* The university provides an Alfresco instance (https://alfresco.lifesci.dundee.ac.uk) (LDAP-based) for collaborating on documents.


* The OME QA system (http://qa.openmicroscopy.org.uk/) is an in-house system for collecting feedback from users, including failing files, stack traces, etc. Like our community feedback, QA feedback should be turned into a ticket in a timely manner.


* Home directory / data repository on necromancer (SSH-based)



Note : *For anyone who has been hired to work at the University of Dundee, you will be provided with another list which itemizes all the things that need to be done to get you setup in RL (building access, a chair, etc.)* See: `new start tasklist`_

Google Docs and Calendars
~~~~~~~~~~~~~~~~~~~~~~~~~

In addition to the services hosted in Dundee, the team also makes use of several Google resources due to the improved real-time collaboration that they provide. A single Google collection “OME Docs” is made available to all team members. Anything placed in the collection is automatically editable by everyone.


For example, the primary contact information for all team members is available in the DevContactList spreadsheet:


    https://spreadsheets.google.com/spreadsheet/ccc?key=0AuHdV7GT-8hmcDBjMldqTEJ4OHRuQVZGbS03UkcwWUE&hl=en_GB#gid=0


.. _devcontactlist_screenshot:
.. figure:: images/10000000000004490000024DCCB6EC99.png
   :align:  center


You can enable notifications on the spreadsheet so that you receive an email if any changes are made.


Similarly, all paper, conference, and release deadlines as well as travel schedules and vacations are put on the “OME Scheduling” calendar

    https://www.google.com/calendar/embed?src=ncf95f8n53mg61b0gdnbu92bhk%40group.calendar.google.com


Meetings
~~~~~~~~

Weekly meetings are held online with all members of the team. Agendas are posted on the appropriate page under


    https://www.openmicroscopy.org/site/community/minutes/conference-calls


before hand. Notes are taken collaboratively in a Google doc in the “OME Docs > Notes” collection. Once finished, they are added to the page on Plone, and anyone who missed the meeting is expected to review the notes and raise any issues during the next meeting. You should also send an email to ome-nitpick if you will not be attending the meeting since it may change what others can discuss for that week.


Periodically, a technical presentation is held during the weekly meeting. This can be used to either introduce an external tool for suggested use by the team or as a peer review of in-progress work.


See https://www.openmicroscopy.org/site/team/meetings for more information.


Minigroup meetings can either be regularly scheduled (e.g. weekly) or on an as-needed basis. Notes from such meetings, however, should be posted centrally to


    https://www.openmicroscopy.org/site/community/minutes/minigroup


.. _minigroups_screenshot:
.. figure:: images/10000000000004490000024DA6F6B2C8.png
   :align:  center

for review by the team. Either an email should be sent to ome-nitpick with a link to the minigroup notes, or it should be brought up during the weekly meeting.




Process summary
---------------

Beyond just seeing *where*, *what*, and *when* things are decided via the collaboration tools above, it’s important to understand *how* and *why* these decisions are made, and what they’re based on.


Each of the process sections below detail a part of the overall process used by the OME team. This is admittedly a lot of information on particulars of how the team works, but since most of the current developers will expect for things to work in this way, it’s far more effective if you can follow along.

Ticket types (Day-to-Day)
~~~~~~~~~~~~~~~~~~~~~~~~~

Any activities on a day-to-day level will be most accurately and actively trackable in the tickets on Trac. Essentially, if no tickets are marked “active” on the whiteboard for a developer, then it’s assumed that s/he is off or working on a non-OME related activity.


Tickets in OME are divided into 3 types:

* Requirements
* Stories
* Tasks


Requirements
^^^^^^^^^^^^

Requirements are large, overarching features which will take months (if not longer) to deliver. For a particular release , or “milestone” in Trac terminology, a small number of requirements will be chosen. For patch releases, it’s possible that no requirements will be in-progress, but that only bug fixing will take place.

Stories
^^^^^^^

Requirements are made up of stories, which should take days to weeks to complete. A large number of stories will be put into any one sprint , the two-week period that is visible on the Trac whiteboard at a given time. This is the standard unit of work for the team. After a sprint, the stories that were chosen for the sprint, should be closed if possible, and there should be some evidence of the work (screenshots, screencasts, etc) available from the milestone page:


    https://trac.openmicroscopy.org.uk/ome/milestone/OMERO-Beta4.4


.. _storyexample_screenshot:
.. figure:: images/10000000000003EF00000209C184C65E.png
   :align:  center

Tasks
^^^^^

Tasks make up stories and are the most basic building block. They should be on the order of 0.25 to 1 day of work, 2 at the most but no lower than 0.1 days. In fact, they are the only type of ticket that contains a field for recording estimated time, and these should be considered
**required**. Sums of such times are then available in the stories and requirements.


The unit of time used by the OME team is “ideal days”. (Note: in some locations in Trac/Agilo an “h” for hour is shown. Regardless, the time unit is ideal days). An ideal day can be thought of as a day on which a single developer can work without interruption for 6 hours, whether this be coding, testing, designing or documenting. Obviously this almost never happens, but it’s simpler to estimate times if a one ignores meetings, mails, and other annoyances.


Beyond the types used in Trac/Agilo, there are several other ways of identifying or specially marking tickets.

Bugs
^^^^

The Agilo plugin provides another potential level to the hierarchy, “Bug,” which could appear in the whiteboard like a story. We have chosen not to use this feature, since it unduly complicates the workflow (e.g. they are treated as container and one must create a bug inside the bug to do anything with it).


Instead, “Bug:” is pre-pended to the ticket summary to indicate a bug. A list of all current such bugs can be viewed via the “BUGS! EEK!!” report in the left hand panel:


    https://trac.openmicroscopy.org.uk/ome/report/8


.. _bugs_screenshot:
.. figure:: images/10000000000003EF0000020903157559.png
   :align:  center

Where possible, we try not to push bugs out of the current milestone, and instead, we aim to handle them as quickly as possible. If a bug is too large to handle during the current milestone, it should be turned into a story and appropriately scheduled.

RFE
^^^

“RFE” stands for “Request for Enhancement” and is a fledgling idea for some new feature. They frequently occur during internal testing. While testing a client, for example, a tester will often have the feeling that it’d be nice to be able to do “X”. A kick ticket with “RFE: add support for X” lets the client developer(s) know that such a feature would be useful. The ticket does not contain the necessary technical details, however, to be a story, though it can be turned into one.

Sprint process (Week-to-week)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sprints begin at one weekly meeting and terminate two weeks later. They consist of tasks that have been marked for the current sprint,


.. _newticket_screenshot:
.. figure:: images/10000000000004490000024D9EE25EC9.png
   :align:  center


all of which then show up on the whiteboard, most of which are grouped together into stories. A story can have some tickets in the current sprint, while others – though in the same milestone – will be handled in a later sprint. For this reason, a sprint should never be set for a story.


In general, the whiteboard at any given time should clearly reflect the team effort. If a requirement is in another milestone but you are working on it ahead of time, then move the current tasks into the current milestone and
sprint so they appear on the whiteboard. (This is a limitation of Trac/Agilo that we are learning to deal with). At certain times, we may have multiple sprints active in which case it’s necessary to be aware of which sprint you are looking at:

.. _whiteboard_screenshot:
.. figure:: images/10000000000004490000024D8FA15AF3.png
   :align:  center


Definition of Done
^^^^^^^^^^^^^^^^^^

For stories to be considered “done”, they should include tests, screenshots/casts, and the definition of any “Testing Scenarios” that may be necessary. If it’s easier for you to remember this, then feel free to add individual tasks inside of the story for the tests, screenshots, etc. Others may prefer to write less granular stories and tickets. The key is that someone who is to review the stories and tasks can clearly decide what has changed and what needs to be reviewed and tested. This often means that each story ticket should contain a long-text description and a “usage” statement ("getting started") along with the related task tickets, and that before it is scheduled into a sprint!

Choosing tasks
^^^^^^^^^^^^^^

Once tasks are placed in a sprint choosing between them is more or less arbitrary. Where possible you should prefer to work on:

* Bugs, since they should be considered top priority


* Risky/unclear changes, since they may have extended impact,


* Tasks that are blocking other developers for obvious reasons, and


* Near the end of the sprint if you have completed your tasks, you should help others complete tasks that they may not be able to complete.


Branch process (Month-to-month)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The output of your daily and weekly work will almost always be the production of a branch. That process is described in (perhaps too much) detail under


    https://trac.openmicroscopy.org.uk/ome/wiki/WorkingWithOmero/UsingGit


Particularly of importance for this document is the section on “Branch management”. The general idea is that branches also have a lifecycle on the project. They begin as **Investigations**, progress to **Works-in-Progress (WIP)**, and eventually become **Deliverables**. Once they are merged into the mainline, they should be removed from github to keep the list of active branches clearly discernible. The **Pull Requests** that are opened by developers are on-going review conversations, which you are encouraged to get involved in.

Release process
~~~~~~~~~~~~~~~

A release is primarily defined on the Trac milestone page, e.g. http://trac.openmicroscopy.org.uk/ome/milestone/OMERO-Beta4.4


.. _milestone_screenshot:
.. figure:: images/10000000000004490000024DBC85F470.png
   :align:  center


All tickets (requirements, stories, and tasks) are reachable via the various green reporting bars. The description highlights what the OME team thinks the most important features and goals for the release are. Each of these large ticket items should also contain a link to the requirements or story ticket.


Major releases consist of some number (10+) of the 2-week sprints described above, and should always end with a test cycle of at least 3 weeks. Smaller bug fix releases may be much shorter and won’t need as extensive testing.

Scenarios
^^^^^^^^^

Testing is largely performed through a number of “scenarios” which are organized on the Trac: https://trac.openmicroscopy.org.uk/ome/wiki/TestingScenarios
Such scenarios should be defined as you develop new features, and the team will periodically review and test the scenarios even before release. So-called “Scenario days” are listed on the front page of the wiki and are typically an all-hands-on deck affair. Numbered scenarios are assigned to individuals and it is best to complete them as quickly as possible.

.. _scenarios_screenshot:
.. figure:: images/10000000000004490000024D99235BBD.png
   :align:  center


Checklist
^^^^^^^^^

A checklist of all the things that should be done as the release date approaches is available under https://trac.openmicroscopy.org.uk/ome/wiki/ReleaseProcess

Yearly meetings
^^^^^^^^^^^^^^^

Typically just before, during, or after a major release, the entire OME team will try to meet to determine the goals and features for the next major release. Being co-located for the release is often also useful in itself, but having time to work through the many different directions is critical. This often happens at the annual users’ meeting in Paris (May/June). For example, the current development period (4.4) has been chosen as “
stability and robustness
”.

Previews
~~~~~~~~

There has been some experimentation on the team with “previews”, which are created and then provided to certain sites for early testing. Previews may be created in the middle of a release or with a final release for testing less stable work.


Specific external groups interested in such previews should be integrated into the process where possible. As soon as previews are ready they should be sent out to interested external parties for testing/review. However, consideration should be taken when choosing such groups since there is a certain amount of indebtedness, i.e. asking a group to test a preview too often could become a burden.

Subgroup processes
~~~~~~~~~~~~~~~~~~

To see how a specific group works together you might take a look at the web process which is defined under ticket 4772: https://trac.openmicroscopy.org.uk/ome/ticket/4772
While numerous new “sub-groups” are getting up-to-speed, we will obviously need to find ways to keep communication and collaboration simple for everyone.

Blogs/etc.:
-----------

* http://scottchacon.com/2011/08/31/github-flow.html
* http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
* http://en.wikipedia.org/wiki/Technical_debt

Satellite collaboration templates:
----------------------------------

* http://dojofoundation.org/about
* http://dojofoundation.org/about/cla
* http://jakarta.apache.org/site/contributing.htm
* http://jakarta.apache.org/site/understandingopensource.html
* http://incubator.apache.org/
* http://www.apache.org/foundation/how-it-works.html


.. _addresses: https://www.openmicroscopy.org/site/team/addresses
.. _new start tasklist: https://www.openmicroscopy.org/site/team/new-start-tasklist

