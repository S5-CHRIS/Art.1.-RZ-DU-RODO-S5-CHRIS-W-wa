---
title: Media Capture and Streams API (Media Stream)
slug: Web/API/Media_Streams_API
tags:
  - API
  - Audio
  - Media
  - Media Capture and Streams API
  - Media Streams API
  - Overview
  - Video
---
{{DefaultAPISidebar("Media Capture and Streams")}}

The **Media Capture and Streams** API, often called the **Media Streams API** or **MediaStream API**, is an API related to [WebRTC](/en-US/docs/Web/API/WebRTC_API) which provides support for streaming audio and video data.

It provides the interfaces and methods for working with the streams and their constituent tracks, the constraints associated with data formats, the success and error callbacks when using the data asynchronously, and the events that are fired during the process.

## Concepts and usage

The API is based on the manipulation of a {{domxref("MediaStream")}} object representing a flux of audio- or video-related data. See an example in [Get the video](/en-US/docs/Web/API/WebRTC_API/Taking_still_photos#get_the_video).

A `MediaStream` consists of zero or more {{domxref("MediaStreamTrack")}} objects, representing various audio or video **tracks**. Each `MediaStreamTrack` may have one or more **channels**. The channel represents the smallest unit of a media stream, such as an audio signal associated with a given speaker, like _left_ or _right_ in a stereo audio track.

`MediaStream` objects have a single **input** and a single **output**. A `MediaStream` object generated by {{domxref("MediaDevices.getUserMedia", "getUserMedia()")}} is called _local_, and has as its source input one of the user's cameras or microphones. A non-local `MediaStream` may be representing a media element, like {{HTMLElement("video")}} or {{HTMLElement("audio")}}, a stream originating over the network, and obtained via the WebRTC {{domxref("RTCPeerConnection")}} API, or a stream created using the [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) {{domxref("MediaStreamAudioDestinationNode")}}.

The output of the `MediaStream` object is linked to a **consumer**. It can be a media elements, like {{HTMLElement("audio")}} or {{HTMLElement("video")}}, the WebRTC {{domxref("RTCPeerConnection")}} API or a [Web Audio API](/en-US/docs/Web/API/Web_Audio_API) {{domxref("MediaStreamAudioSourceNode")}}.

## Interfaces

In these reference articles, you'll find the fundamental information you'll need to know about each of the interfaces that make up the Media Capture and Streams API.

- {{domxref("BlobEvent")}}
- {{domxref("CanvasCaptureMediaStreamTrack")}}
- {{domxref("InputDeviceInfo")}}
- {{domxref("MediaDeviceKind")}}
- {{domxref("MediaDeviceInfo")}}
- {{domxref("MediaDevices")}}
- {{domxref("MediaStream")}}
- {{domxref("MediaStreamConstraints")}}
- {{domxref("MediaStreamEvent")}}
- {{domxref("MediaStreamTrack")}}
- {{domxref("MediaStreamTrackEvent")}}
- {{domxref("MediaTrackCapabilities")}}
- {{domxref("MediaTrackConstraints")}}
- {{domxref("MediaTrackSettings")}}
- {{domxref("MediaTrackSupportedConstraints")}}
- {{domxref("NavigatorUserMedia")}}
- {{domxref("NavigatorUserMediaError")}}
- {{domxref("OverconstrainedError")}}
- {{domxref("URL")}}

Early versions of the Media Capture and Streams API specification included separate `AudioStreamTrack` and `VideoStreamTrack` interfaces—each based upon {{domxref("MediaStreamTrack")}}—which represented streams of those types. These no longer exist, and you should update any existing code to instead use `MediaStreamTrack` directly.

## Events

- {{event("addtrack")}}
- {{event("ended")}}
- {{event("muted")}}
- {{event("overconstrained")}}
- {{event("removetrack")}}
- {{event("started")}}
- {{event("unmuted")}}

## Guides and tutorials

The articles below provide additional guidance and how-to information that will help you learn to use the API, and how to perform specific tasks that you may wish to handle.

{{LandingPageListSubpages}}

## Browser compatibility

{{Compat("api.MediaStream")}}

## See also

- [WebRTC](/en-US/docs/Web/API/WebRTC_API) - the introductory page to the API
- {{domxref("mediaDevices.getUserMedia()")}}
- [Taking still photos with WebRTC](/en-US/docs/Web/API/WebRTC_API/Taking_still_photos): a demonstration and tutorial about using `getUserMedia()`.