# StethoForVolley
Volley 1.1.0 Network Call Inspection library for Stetho.

Inspect your volley network requests without OkHttp Layer using Stetho Url-Connection.

# Usage

To use it, add the following lines in build.gradle

Step 1. Add it in your root build.gradle at the end of repositories:
```gradle
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
Step 2. Add the dependency
```gradle
dependencies {
   implementation 'com.github.darshan-kapasi:StethoForVolley:1.0'
}
```
# Inspecting Volley Request

1) Add a new instance of `StethoVolleyStack` while creating `RequestQueue` for your volley request

```java
RequestQueue queue = Volley.newRequestQueue(this, new StethoVolleyHurlStack());
```

That's all. Run the app and you can inspect your request and response from chrome://inspect/
