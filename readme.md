## How to reproduce the issue

```
~/git/dotty-issues ⑂master* $ sbt
...
sbt:dotty-cross> ++ 2.12.10
...
sbt:dotty-cross> compile
...
[success] Total time: 3 s, completed Oct 12, 2019, 7:09:08 PM
sbt:dotty-cross> ++ 0.19.0-RC1
...
sbt:dotty-cross> compile
[info] Updating ...
[info] Done updating.
[info] Compiling 1 Scala source to /Users/apipicello/git/dotty-issues/target/scala-0.19/classes ...
[error] -- [E007] Type Mismatch Error: /Users/apipicello/git/dotty-issues/src/main/scala/DepTest.scala:9:28
[error] 9 |  Dep(obj).fun(obj.Dependent())
[error]   |               ^^^^^^^^^^^^^^^
[error]   |               Found:    DepTest.obj.Dependent
[error]   |               Required: Nothing
[error] one error found
[error] (Compile / compileIncremental) Compilation failed
[error] Total time: 2 s, completed Oct 12, 2019, 7:09:28 PM
sbt:dotty-cross>
```
