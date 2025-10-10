---
title: "documentAttributeVideo"
description: "Defines a video"
nav_exclude: true
image: https://docs.madelineproto.xyz/favicons/android-chrome-256x256.png
---
# Constructor: documentAttributeVideo  
[Back to constructors index](/API_docs/constructors/index.html)



Defines a video

### Attributes:

| Name     |    Type       | Required | Description |
|----------|---------------|----------|-------------|
|round\_message|[Bool](/API_docs/types/Bool.html) | Optional|Whether this is a round video|
|supports\_streaming|[Bool](/API_docs/types/Bool.html) | Optional|Whether the video supports streaming|
|nosound|[Bool](/API_docs/types/Bool.html) | Optional|Whether the specified document is a video file with no audio tracks|
|duration|[double](/API_docs/types/double.html) | Optional|Duration in seconds|
|w|[int](/API_docs/types/int.html) | Optional|Video width|
|h|[int](/API_docs/types/int.html) | Optional|Video height|
|preload\_prefix\_size|[int](/API_docs/types/int.html) | Optional|Number of bytes to preload when preloading videos (particularly [video stories](https://core.telegram.org/api/stories)).|
|video\_start\_ts|[double](/API_docs/types/double.html) | Optional|Floating point UNIX timestamp in seconds, indicating the frame of the video that should be used as static preview and thumbnail.|
|video\_codec|[string](/API_docs/types/string.html) | Optional|Codec used for the video, i.e. "h264", "h265", or "av1"|



### Type: [DocumentAttribute](/API_docs/types/DocumentAttribute.html)


### Example:

```
$documentAttributeVideo = ['_' => 'documentAttributeVideo', 'round_message' => Bool, 'supports_streaming' => Bool, 'nosound' => Bool, 'duration' => double, 'w' => int, 'h' => int, 'preload_prefix_size' => int, 'video_start_ts' => double, 'video_codec' => 'string'];
```  
