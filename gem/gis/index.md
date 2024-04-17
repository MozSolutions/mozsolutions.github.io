---
title: Gem GIS
description: Gem Geographical Information System
---
*Information Level*

Rox Camera Provider acquires images with the device camera using native platform components.

*Rox Camera Provider for Xamarin.Forms supports Android, iOS, and UWP*.

The Rox Camera Provider has the following methods:

```csharp
    //Take a picture with the device camera
    Task<ImageSource> AcquirePicture();
```

## Platform Considerations

### Android

In your Android project `MainActivity.cs` code file, you must call `Rox.Camera.Init(Activity)` before `Xamarin.Forms.Forms.Init()`. It should look something like:

```csharp
    global::Rox.Camera.Init(this);

    global::Xamarin.Forms.Forms.Init();

    LoadApplication(new MyCameraApplication());
```

### iOS

In your iOS project `AppDelegate.cs` code file, you must call `Rox.Camera.Init()` before `Xamarin.Forms.Forms.Init()`. It should look something like:

```csharp
    global::Rox.Camera.Init();

    global::Xamarin.Forms.Forms.Init();

    LoadApplication(new MyCameraApplication());
```

---
©2016-2024 [*`Moz Solutions`*](/)
