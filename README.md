# Migration builds

ClassicPress nightly **migration** builds will live in this branch.

A **migration** build is a build for use by the migration plugin:
https://github.com/ClassicPress/ClassicPress-Migration-Plugin

The migration builds are slightly different from the regular ClassicPress
builds.  All files in a migration build need to be contained within a top-level
folder of `wordpress`.

This is because one of the first things the WordPress update process does is
extract the file `/wordpress/wp-admin/includes/update-core.php` from the new
update package:

https://nylen.io/wp/4.9.8/src/wp-admin/includes/class-core-upgrader.php#L133-L139

So there needs to be a file in the update package with that exact path and
name.  After that, the ClassicPress code takes over and finishes the migration.

## And an easter egg

This file is going to be removed when the first automated migration build is
committed.  So if you're reading this, I'll buy you a beer.

Or at least send you a beer emoji
[on Slack, after you join](https://www.classicpress.net/get-involved/).

Here's a message you can use:

> Hey @James Nylen, I saw your initial commit on the `migration` branch of
> https://github.com/ClassyBot/ClassicPress-nightly.  Do I get a prize?
