#### A sample android app with Go bindings

* Install `gomobile` and  android compiler toolchain.
* Set `GOPATH` and `GOROOT` env variables.
* Build android library (.aar) project from your
Go source using `gobind` tool.

```
$ cd GopherAndy
$ go get -u golang.org/x/mobile/cmd/gomobile && gomobile init

$ ./gradlew -b gobuild/build.gradle gobind
or
$ gomobile bind -target=android github.com/sureshg/hello

```
* Import the golang library (`gobuild/gobuild.aar`) to your android project.

```java
import go.hello.Hello;
...
Hello.Greetings("Hello from Java!");
```

### For more details

* https://github.com/golang/go/wiki/Mobile
* https://github.com/golang/mobile/tree/master/example/bind
* https://plugins.gradle.org/plugin/org.golang.mobile.bind




