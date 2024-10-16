[![JitPack](https://img.shields.io/badge/JitPack-1.0.0-brightgreen.svg?style=for-the-badge)](https://jitpack.io/#debacodex/segmented-control)        

[![Blogger](https://img.shields.io/badge/Blogger-FF5722?style=for-the-badge&logo=blogger&logoColor=white)](https://debacodes.blogspot.com)   

[![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/mr.deba.000?mibextid=ZbWKwL)


# android-segmented-control

=========================
Android-Segmented is a custom view for Android which is based on RadioGroup and RadioButton widget.
This implementation is inspired by [Segmented Controls](https://developer.apple.com/library/ios/documentation/userexperience/conceptual/UIKitUICatalog/UISegmentedControl.html) for iOS.

![Sample Image](https://raw2.github.com/hoang8f/android-segmented-control/master/screenshot/screenshot.png)

## Including in your project


#### Using maven
Android-Segmented Library is pushed to [Maven Central](http://search.maven.org/#search|ga|1|android-segmented), so you just need to add the following dependency to your `build.gradle`.

    dependencies {
        implementation 'com.github.debacodex:segmented-control:1.0.0'
    }
    
    
    Then you need to add jitpack as your maven repository in `build.gradle`  file:

```groovy
repositories {
    google()
    jcenter()
    maven { url 'https://jitpack.io' }
}
```

#### Manually
Copy(or merge) below files into corresponding file/folder:
  + SegmentedGroup.java
  + res/drawable/*
  + res/drawable-v14/*
  + res/values/colors.xml
  + res/values/dimens.xml
  + res/values/styles.xml (only RadioButton style)

Usage
-----
Define in xml like this and make sure that the `RadioButton`'s style is: `@style/RadioButton`

```xml
<info.hoang8f.android.segmented.SegmentedGroup
    android:id="@+id/segmented2"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_margin="10dp"
    android:orientation="horizontal">

    <RadioButton
        android:id="@+id/button21"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="One"
        style="@style/RadioButton" />

    <RadioButton
        android:id="@+id/button22"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Two"
        style="@style/RadioButton" />
</info.hoang8f.android.segmented.SegmentedGroup>
```

You also can be change the tint color and title color when button is checked by `setTintColor` method.
Here is sample code:

```java
SegmentedGroup segmented2 = (SegmentedGroup) rootView.findViewById(R.id.segmented2);
segmented2.setTintColor(Color.DKGRAY);

SegmentedGroup segmented3 = (SegmentedGroup) rootView.findViewById(R.id.segmented3);
segmented3.setTintColor(Color.parseColor("#FFD0FF3C"), Color.parseColor("#FF7B07B2"));

SegmentedGroup segmented4 = (SegmentedGroup) rootView.findViewById(R.id.segmented4);
segmented4.setTintColor(getResources().getColor(R.color.radio_button_selected_color));
```

Credits
-------
Author: Le Van Hoang (@debacodex)

License
-------
    The MIT License (MIT)
    
    Copyright (c) 2014 Le Van Hoang
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.



