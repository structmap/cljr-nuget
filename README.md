# cljr-nuget

ClojureCLR utility for adding NuGet-hosted libraries to the AssemblyLoadContext at runtime

## usage

```
cljr -Sdeps '{:deps {io.github.structmap/cljr-nuget {:git/tag "v0.0.1"  :git/sha "d00c5a7"}}}'
(require '[structmap.loader :as loader])
(loader/assembly-load "AWSSDK.Core")
(loader/assembly-load "AWSSDK.S3")
```

## warning

This is hacky utility code not even pre-alpha. Do not use!
