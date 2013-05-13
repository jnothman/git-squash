git-squash
==========

Tool to squash the current branch/HEAD and rebase it onto a given commit.

This calls ``git rebase -i``, but automatically replaces all but the first
``pick`` entry to ``squash``.

If the rebase is trivial (e.g. the base is an ancestor of the current HEAD) and
does not require interactive conflict resolution, ``git squash`` will also set
the commit message.

Requirements: ``bash``, ``awk``, ``grep`` with PCRE support, and of course
``git``, and a set ``EDITOR`` environment variable.

Installation: copy the git-squash file to a directory on your ``PATH`` and ``chmod +x``.

Usage::

    git squash [-m <commit msg>] <base>
