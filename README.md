### Android StyleableToast

An Android library that takes the standard Android Toast and takes it to the next level with a variety of styling options that gives your app and user experience that little extra unique feeling!


Currently used in:
- [Quote Creator] (https://play.google.com/store/apps/details?id=org.m.muddzboy.QuoteCreator&hl=da) with +80.000 downloads!
- [Shoppist] (https://play.google.com/store/apps/details?id=com.muddii.shopping_list&hl=da)

*Feel free to contact me if you want your app to be included here*

<a href="https://github.com/Muddz/StyleableToast/raw/master/sample.apk">Download the sample .apk: </a>


### Features

- Style toasts in a styles.xml or from code.
- Set background color of the toast.
- Set the corner radius of the toast and archive different shapes.
- Set the transparency of your toast to get full solid or transparent toast.
- Set stroke width and color on your toast.
- Style the toast text with a text color or bold.
- Set a new font for the toast text.
- Set a icon beside the toast text.
- Set an spinning animation effect on your icon (see below example)
- Works from Api 16+

*(Next version: Builder pattern, elevtion and toast size)*

## CASES:
![alt tag](https://github.com/Muddz/StyleableToast/blob/master/styleable%20cases.png)

## With spinIconAnimation(); method:
![alt tag](https://media.giphy.com/media/hoq66naJQkECI/giphy.gif)

----

### Usage with a style resource:


**1) Style your toast in styles.xml. All available attributes:**

    <style name="StyledToast">

        <item name="android:textColor"></item>
        <item name="android:textStyle"></item>
        <item name="android:fontFamily"></item>
        <item name="android:colorBackground"></item>
        <item name="android:strokeWidth"></item> // API 21+
        <item name="android:strokeColor"></item> // API 21+
        <item name="android:radius"></item>
        <item name="android:alpha"></item>
        <item name="android:icon">/</item>
        
    </style>

**2) Pass your style resource in the constructor and call show();**

    StyleableToast.makeText(context, "Saving profile", Toast.LENGTH_LONG, R.style.StyledToast).show();
    
### Usage with by code:

                StyleableToast st = new StyleableToast(this, "Updating profile", Toast.LENGTH_SHORT);
                st.setBackgroundColor(Color.parseColor("#ff5a5f"));
                st.setTextColor(Color.WHITE);
                st.setIcon(R.drawable.ic_autorenew_black_24dp);
                st.spinIconAnimation();
                st.setAlpha(StyleableToast.MAX_VISIBILTY);
                st.show();
-----
    
### Installation

Add the depedency in your build.gradle. The library is distributed via jCenter

```groovy
dependencies {
    compile 'com.muddzdev:styleabletoast:1.0.3'   
}
```
 ----

### License

    Copyright 2017 Muddii Walid (Muddz)

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.