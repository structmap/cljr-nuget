# cljr-nuget

ClojureCLR utility for adding NuGet-hosted libraries to the AssemblyLoadContext at runtime

## deprecation

The goal of this tool was to make it easier to bring NuGet-packaged libraries into a Clojure REPL context.

I have since found that a better way to procure libraries is to start from the traditional csproj / msbuild enviornment and from there launch into the Clojure REPL context.

Here is an example project that shows this approach: https://github.com/jamesdavidson/prebuild-example

## usage

```
cljr -Sdeps '{:deps {io.github.structmap/cljr-nuget {:git/tag "v0.0.3"  :git/sha "ffad286"}}}'
(require '[structmap.nuget :as nuget])
(nuget/default-load "AWSSDK.Core")
(nuget/default-load "AWSSDK.S3")
```

## warning

This is hacky utility code not even pre-alpha. Do not use!
