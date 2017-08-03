##  Live
A Rx Transformer handling Android Lifecycle in the  same way with LiveData.

if you just want to take the stream until a specific lifecycle event happen, maybe <a href = "https://github.com/trello/RxLifecycle">RxLifecycle</a> is that you really want.

## Usage

```java

public class MainActivity extends LifecycleActivity {

    protected void onCreate(Bundle savedInstanceState) {

        mObservable
                .compose(Live.bindLifecycle(this))
                .subscribe();

    }
}

```

## Installation

```groovy
allprojects {
    repositories {
        maven { url 'https://maven.google.com' }
        jcenter()
    }
}
```

```groovy
compile 'com.shundaojia:live:0.1.1'
```