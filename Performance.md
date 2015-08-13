> We tested the performance of MTFS which is mounted over a Lustre cluster, and got the following results.

  * Sequential Write, which shows that write performance declines about 28% at most when MTFS have two branches.

> <img src='http://mtfs.googlecode.com/files/Write%20Performance.jpg' alt='' />

  * Random Write, which shows that random write performance declines about 21% at most when MTFS have two branches.

<img src='http://mtfs.googlecode.com/files/Ramdom%20Write%20Performance.jpg' alt='' />

  * Sequential Read, which shows that read performance of MTFS is basically the same with Lustre.

<img src='http://mtfs.googlecode.com/files/Read%20Performance.jpg' alt='' />

  * Random Read, which which shows that random read performance of MTFS is basically the same with Lustre.

<img src='http://mtfs.googlecode.com/files/Random%20Read%20Performance.jpg' alt='' />