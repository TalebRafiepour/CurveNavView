# CurveNavView

NavigationView from android design support library with curved edge

# Usage

```xml
<android.support.v4.widget.DrawerLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/drawer_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:fitsSystemWindows="true"
    tools:openDrawer="start">
    
    ...
    
    <com.rom4ek.curvenavview.CurveNavView
        android:id="@+id/nav_view"
        android:layout_width="wrap_content"
        android:layout_height="match_parent"
        android:layout_gravity="start"
        android:background="@android:color/white"
        android:fitsSystemWindows="true"
        app:itemBackground="@android:color/white"
        app:headerLayout="@layout/nav_header_main"
        app:menu="@menu/activity_main_drawer"
        app:curveCropDirection="cropOutside|cropInside"
        app:fontAssetSrc="fonts/TT0998M_.ttf"
        app:curveWidth="96dp"/>
</android.support.v4.widget.DrawerLayout>
```

# Sample

## Crop Outside

```xml
<android.support.v4.widget.DrawerLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/drawer_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:fitsSystemWindows="true"
    tools:openDrawer="start">
    
    ...
    
    <com.rom4ek.curvenavview.CurveNavView
        android:id="@+id/nav_view"
        android:layout_width="wrap_content"
        android:layout_height="match_parent"
        android:layout_gravity="start"
        android:background="@android:color/white"
        android:fitsSystemWindows="true"
        app:itemBackground="@android:color/white"
        app:headerLayout="@layout/nav_header_main"
        app:menu="@menu/activity_main_drawer"
        app:curveCropDirection="cropOutside"
        app:curveWidth="96dp"/>
</android.support.v4.widget.DrawerLayout>
```



## Crop Inside

```xml
<android.support.v4.widget.DrawerLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/drawer_layout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:fitsSystemWindows="true"
    tools:openDrawer="start">
    
    ...
    
    <com.rom4ek.curvenavview.CurveNavView
        android:id="@+id/nav_view"
        android:layout_width="wrap_content"
        android:layout_height="match_parent"
        android:layout_gravity="start"
        android:background="@android:color/white"
        android:fitsSystemWindows="true"
        app:itemBackground="@android:color/white"
        app:headerLayout="@layout/nav_header_main"
        app:menu="@menu/activity_main_drawer"
        app:curveCropDirection="cropInside"
        app:curveWidth="96dp"/>
</android.support.v4.widget.DrawerLayout>
```
<img src="https://raw.githubusercontent.com/rom4ek/CurveNavView/master/media/crop_inside.png" width="303">


## Translucent status or navigation bar

Simply add next lines to your ```styles-v21``` folder

```xml
<style name="AppTheme" parent="AppTheme.Base">
    <item name="android:windowTranslucentNavigation">true</item>
    <item name="android:windowTranslucentStatus">true</item>
</style>
```

# Download
In your module's build.gradle file:

```gradle

allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}


dependencies {
    implementation 'com.github.TalebRafiepour:CurveNavView:0.0.1'
}
```