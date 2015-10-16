#### A sample android app with Go bindings

* Install `gomobile` and  android compiler toolchain.
* Set `GOPATH` and `GOROOT` env variables.
* Build android library (.aar) project from your
Go source using `gobind` tool.

```
$ cd GopherAndy
$ go get -u golang.org/x/mobile/cmd/gomobile && gomobile init
$ ./gradlew -b gobuild/build.gradle gobind

```
* Import the golang library project (`gobuild/gobuild.aar`)

```java
import go.hello.Hello;
...
Hello.Greetings("Hello from Java!");
```



