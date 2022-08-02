FAQ
###

Here are some answers to frequently-asked questions.
Got a question that isn't answered here? You can `write <mailto:support@flomics.com>` to us and we will answer as fast as we can!

.. contents::
    :local:
    :depth: 2


How do I…
=========

.. _move:

…rename my files according to a new path format configuration?
--------------------------------------------------------------

Just run the :ref:`move-cmd` command. Use a :doc:`query </reference/query>`
to rename a subset of your music or leave the query off to rename
everything.

Why does beets…
===============

.. _nomatch:

…complain that it can't find a match?
-------------------------------------

There are a number of possibilities:

-  First, make sure the album is in `the MusicBrainz
   database <https://musicbrainz.org/>`__. You
   can search on their site to make sure it's cataloged there. (If not,
   anyone can edit MusicBrainz---so consider adding the data yourself.)
-  If the album in question is a multi-disc release, see the relevant
   FAQ answer above.
-  The music files' metadata might be insufficient. Try using the "enter
   search" or "enter ID" options to help the matching process find the
   right MusicBrainz entry.
-  If you have a lot of files that are missing metadata, consider using
   :doc:`acoustic fingerprinting </plugins/chroma>` or
   :doc:`filename-based guesses </plugins/fromfilename>`
   for that music.

If none of these situations apply and you're still having trouble
tagging something, please :ref:`file a bug report <bugs>`.


