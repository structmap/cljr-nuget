# cljr-nuget

ClojureCLR utility for adding NuGet-hosted libraries to the AssemblyLoadContext at runtime

## usage

```
cljr -Sdeps '{:deps {io.github.structmap/cljr-nuget {:git/tag "v0.0.3"  :git/sha "ffad286"}}}'
(require '[structmap.nuget :as nuget])
(nuget/default-load "AWSSDK.Core")
(nuget/default-load "AWSSDK.S3")
```

## warning

This is hacky utility code not even pre-alpha. Do not use!
