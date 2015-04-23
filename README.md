# DiskCacheAndroid
Simple and Fast Cache for Android

----------------------------------

DiskCache is a beautiful lib to works with cache in android, simple, quick and good.

See examples :

## INSTANCE , is Easy ##

```
DiskCache diskCache = DiskCache.get(getApplicationContext());
```
## PUT 
```
//Can put String, Object, SerializableValue, Binary, 
//JSONObject, Drawable,Bitmap
diskCache.put("key","foo");

//Put with time to expire , save for one day , 
//and after expire time returns null
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


## REMOVE 
```
diskCache.remove("key","foo");
```

##ADVANCED

```
//put the size of cache - default is 50MB

private static final int MAX_SIZE = 1000 * 1000 * 50;  // 50MB
private static final int MAX_COUNT = Integer.MAX_VALUE; // max objects can be saved

DiskCache diskCache = DiskCache.get(getApplicationContext(),MAX_SIZE,MAX_COUNT);
```