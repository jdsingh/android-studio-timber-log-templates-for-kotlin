# Android Studio Timber Log Templates for Kotlin

Android Studio provides 'Live Templates' for inserting recurring code snippets like loops and log statements. For example, hitting TAB when entering `logd` will produce

```java
    Log.d("divide: foo");
 ```
 
Not all templates are available for Kotlin, yet. To spare you the time of creating them, this repo provides the Kotlin version of the timber log templates.

# Download

* Download [templates/settings.jar](/templates/settings.jar) and import it in Android Studio via 'File > Import Settings...'

OR

* Download [templates/AndroidLogKotlin.xml](/templates/AndroidLogKotlin.xml) and move it into Android Studio's `templates` directory (on Windows: C:\Users\John\\.AndroidStudio3.1\config\templates)

The templates will be available after restarting Android Studio.

# Usage

## logd - Timber.d(String)

```kotlin
    Timber.d("divide: foo")
```
    
## loge - Timber.e(Exception, String)

```kotlin
    Timber.e(e, "divide: foo")
```

## logi - Timber.i(String)

```kotlin
    Timber.i("divide: foo")
```

## logm - Log method name and its arguments

```kotlin
    Timber.d("divide() called with: a = [$a], b = [$b]")
```

## logr - Log result of this method

```kotlin
    Timber.d("divide() returned: $result")
```
    
## logw - Log.w(Exception, String)

```kotlin
    Timber.w(e, "divide: foo")
```
    
## wtf - Log.wtf(Exception, String)


```kotlin
    Timber.wtf(e, "divide: foo")
```

**Note:** Any changes you've made to the Java log templates will get lost as the 'AndroidLog.xml' file is overwritten. You can prevent this by merging the XML files manually.

The templates will be available after restarting Android Studio.

# Modify Templates

One can edit these templates and add new ones in Android Studio under 'Settings > Editor > Live Templates'.

Also, you can restore the built-in templates there if any problems occur after the import.
