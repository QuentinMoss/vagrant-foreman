# TODO

 - [ ] Use `hammer` to create an architecture (x86_64).
 - [ ] Use `hammer` to create an OS ([CentOS 7.2.1511 Minimal][centos7-iso]).

Example:

```
$ hammer architecture create --name x86_64
$ hammer os create --name "CentOS 7" --major 7 --minor 2
$ hammer medium create --name "CentOS 7.2.1511 Minimal" --path https://mirrors.kernel.org/.../.iso
```

Then associate all of these things together and you'll have something ready to go.

 [centos7-iso]: https://mirrors.kernel.org/centos/7.2.1511/isos/x86_64/CentOS-7-x86_64-Minimal-1511.iso
