# WDX Lab: Kotlin Events

Event Emitter for Kotlin

## Installation

```
repositories {
  maven {
    url  "https://dl.bintray.com/wdxlab/maven" 
  }
}

dependencies {
  implementation 'com.wdxlab.events:events:{version}'
}
```

## Usage

```kotlin
import com.wdxlab.events.Event

class Foo {
  val event = Event<Sender, Arg>()
}

val foo = Foo()

foo.event.on { sender, arg -> /* do something with sender and arg */ }
foo.event.emit(someSender, someArg)
```