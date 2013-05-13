git-squash
==========

Tool to squash the current branch/HEAD and rebase it onto a given commit.

Usage::

    git squash [-m <commit msg>] <base>

This calls ``git rebase -i``, but automatically replaces all but the first
``pick`` entry with ``squash``.

If the rebase is trivial (e.g. _base_ is an ancestor of the current HEAD) and
does not require interactive conflict resolution, ``git squash`` can also set
the commit message.

Requirements: ``bash``, ``awk``, ``grep`` with PCRE support, and of course
``git`` >= 1.7.8, and a set ``EDITOR`` environment variable.

Installation: copy the git-squash file to a directory on your ``PATH`` and ``chmod +x``.
