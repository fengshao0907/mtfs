# Introduction #

Roadmap of MTFS.


# Details #

0.0 Versions for prototype design.
  * Append write problems.
  * Online check for async\_replication.
  * Online check for directories.
  * Disk space problems.
  * Lock mode converting.
  * Self-heal.
  * Async replication for multi branches.

0.1 Versions for local filesystems.
  * Flag based updating.
  * General lower file system layer.
  * Journal based recovery.

0.2 Versions for distributed filesystems.
  * Supports for Lustre, NFS and many other file systems.
  * Distributed flag.
  * Updating based on distributed lock (for Lustre).

0.3 Versions for new subjects.
  * Cache subject based on tmpfs.
  * File system speed-up for SSD.
  * Online branch switching.

0.4 Versions for performance tuning.
  * Intergrated benckmarks.
  * Thread number tuning.

1.0 Stable releases for async replication.
  * Common layers for both sync and async replication.

2.0 Versions for archive backup.
  * General file layout layer.
  * Data de-duplication.
  * Compress replication.