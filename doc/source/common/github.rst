#######################################
Introduction to Gerrit for GitHub users
#######################################

.. note::

  This section is intended as a Gerrit quickstart for people who are
  already familiar with code review via GitHub.  It covers the primary
  conceptual and architectural differences between the two services.
  In order to submit reviews, you will need to complete the :doc:`git`
  and :doc:`setup-gerrit` guides.

High-level design and concepts
==============================

Users of GitHub will be familiar with the concept of `pull requests
<https://help.github.com/articles/about-pull-requests/>`_ as the
primary unit of change which is submitted for review.  A pull request
encapsulates one or more git commits and submits the commit(s) for
review along with an additional title and a description.

In contrast, in Gerrit each review consists of a single commit,
therefore the title and description of the change come directly from
the commit message.

Another key difference is that in GitHub pull requests are uniquely
identified by a triple consisting of

1. the user or organization from whence the change originated,
2. the name of the repository it is being submitted to, and
3. an integer representing the pull request's id

whereas Gerrit uses a `post-commit hook
<https://git-scm.com/docs/githooks#_post_commit>`_ to automatically
append a line like::

    Change-Id: Iea9622fff58cf5c8806f5ae59198245902632551

to each commit message.  Gerrit uses this unique id to refer to the
commit, and it will be preserved even if the commit is rebased or its
changes are modified in some way.


Initial setup
=============

Please see the :doc:`setup-gerrit` guide.


Submitting changes for review
=============================



Finding changes to review
=========================


Reviewing changes
=================

  https://docs.openstack.org/infra/manual/developers.html#code-review


Amending changes
================

Merging changes
===============

CI
==
