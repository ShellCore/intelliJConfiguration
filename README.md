# Elementos agregados a IntelliJ Android Studio

## Live templates

### Libraries (gradle)

- butterknife : Butterknife library (View injection)
```groovy
compile 'com.jakewharton:butterknife:8.4.0'
apt 'com.jakewharton:butterknife-compiler:8.4.0'
```

- cardview : google cardview library (View elements)
```groovy
compile 'com.android.support:cardview-v7:+'
```

- circleimageview : Circle Image View library (View elements)
```groovy
compile 'de.hdodenhof:circleimageview:+'
```

- cloudinary : Cloudinary library (Web service to store images in the cloud)
```groovy
compile 'com.cloudinary:cloudinary-android:1.1.2'
```

- dagger : Dagger library (Dependence injection)
    - classpath (Proyect build.gradle > buildscript > dependencies):
        ```groovy
        classpath 'com.neenbedankt.gradle.plugins:android-apt:1.8'
        ```
    - plugin (app build.gradle):
        ```groovy
        apply plugin: 'com.neenbedankt.android-apt'
        ```

    - dependencies (app build.gradle > dependencies):
        ```groovy
        apt 'com.google.dagger:dagger-compiler:2.0.1'
        compile 'javax.annotation:jsr250-api:1.0'
        compile 'com.google.dagger:dagger:2.0.1'
        ```

- dbflow : DBFlow library (DataBase ORM)
```groovy
apt 'com.github.Raizlabs.DBFlow:dbflow-processor:+'
compile 'com.github.Raizlabs.DBFlow:dbflow-core:+'
compile 'com.github.Raizlabs.DBFlow:dbflow:+'
```

- design : Design Library (View elements)
```groovy
compile 'com.android.support:design:+'
```

- eventbus : Eventbus library (Event manager by GreenRobot)
```groovy
compile 'org.greenrobot:eventbus:3.0.0'
```

- facebook : Facebook library (Facebook Web service to authenticate)
```groovy
compile 'com.facebook.android:facebook-android-sdk:[4,5)'
```

- firebase : Firebase services
    - auth:
        ```groovy
        compile 'com.google.firebase:firebase-auth:+'
        ```
    - database:
        ```groovy
        compile 'com.google.firebase:firebase-database:+'
        ```

- glide : Glide library (Image manager)
    ```groovy
    compile 'com.github.bumptech.glide:glide:+'
    ```

- recyclerview : Recycler View library (View element)
```groovy
compile 'com.android.support:recyclerview-v7:+'
```

- retrofit : Retrofit Library (REST service framework)
    ```groovy
    compile 'com.squareup.retrofit2:converter-gson:+'
    compile 'com.squareup.retrofit2:retrofit:+'
    ```

### Java

- provide : Code to add provide function in a Module class
```java
@dagger.Provides
@javax.inject.Singleton
$CLASS$ provides$CLASS$() {
    return $0$;
}
```

- snackbar : Code to add a Snackbar in an Activity
```java
android.support.design.widget.Snackbar.make($container$, $message$, Snackbar.LENGTH_SHORT)
        .show();
```
- http3.login : Login interceptor in HTTP3 (Works with retrofit to add login credentials in the services)
```java
compile 'com.squareup.okhttp3:logging-interceptor:3.8.0'
```java