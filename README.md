# glog

[![PkgGoDev](https://pkg.go.dev/badge/github.com/goduang/glog)](https://pkg.go.dev/github.com/goduang/glog)

Leveled execution logs for Go.

**Forked from golang/glog, removed the annoying flags and allowed setting log verbosity level.**

This is an efficient pure Go implementation of leveled logs in the
manner of the open source C++ package [_glog_](https://github.com/google/glog).

The comment from `glog.go` introduces the ideas:

Package _glog_ implements logging analogous to the Google-internal C++ INFO/ERROR/V setup.  It provides the functions Info, Warning, Error, Fatal, plus formatting variants such as Infof. It also provides V-style loggingcontrolled by the `glog.InitLogs(level)` function.

Basic examples:

```go
glog.InitLogs(3)
defer glog.Flush()

glog.Info("Prepare to repel boarders")

glog.Fatalf("Initialization failed: %s", err)
```

See the documentation for the V function for an explanation of these examples:

```go
if glog.V(2) {
	glog.Info("Starting transaction...")
}
glog.V(2).Infoln("Processed", nItems, "elements")
```

The repository contains an open source version of the log package used inside Google. The master copy of the source lives inside Google, not here. The code in this repo is for export only and is not itself under development. Feature requests will be ignored.

Send bug reports to golang-nuts@googlegroups.com.
