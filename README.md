md5 Implemented in Bash
=======================

Pure Bash implementation of the MD5 checksum algorithm. The hash is computed
entirely with Bash builtins; the implementation does not invoke external
utilities.

The hot path bulk-decodes input, stores message words in scalar variables, and
evaluates all 64 MD5 rounds as one fully unrolled arithmetic command. This is
intentionally optimized for throughput rather than readability.

Usage
----

```
./md5 file.txt
./md5 < file.bin
echo 'hello' | ./md5
DEBUG=1 ./md5 file.txt
```

YouTube
-------

Watch me build this live on YouTube.

<a href="https://www.youtube.com/watch?v=VDQmu6KzDvU"><img alt="Bash md5 YouTube
Thumbnail" src="https://files.daveeddy.com/ysap/bash-md5-thumbnail.jpg"
/></a>

License
-------

MIT License
