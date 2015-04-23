# DiskCacheAndroid
Simple and Fast Cache for Android

----------------------------------


DiskCache is a beautiful lib to works with cache in android, simple, quick and good.

See examples :

## SIMPLE MODE ##

```
DiskCache diskCache = DiskCache.get(getApplicationContext());
```
## PUT ## 
```
//Can put String, Object, SerializableValue, Binary, JSONObject, Drawable,Bitmap
diskCache.put("key","foo");

//Put with time to expire , save for one day and expire after that returns null
diskCache.put("key","foo", DiskCache.TIME_DAY*1);

//hour time
diskCache.put("key","foo", DiskCache.TIME_MINUTE*1);
```

## GET ##
```
diskCache.get("key");
diskCache.getAsString("key");
diskCache.getAsObject("key");
diskCache.getAsBinary("key");
diskCache.getAsJSONObject("key");
diskCache.getAsDrawable("key");
diskCache.getAsBitmap("key");
diskCache.getAsBinary("key");
```