# Crash on cc_library in constraint values attribute

In Bazel 8.0.0-pre.20240618.2, adding a `cc_library` target to the
`constrain_value`s of a `platform` causes Bazel to crash. To reproduce, run

```
bazelisk build --platforms=//:platform :binary
```
