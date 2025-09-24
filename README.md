# RTSP Streaming with MediaMTX and hls.js

This example demonstrates how to play an RTSP stream on the web using **MediaMTX** and **hls.js**.

## 1. Download MediaMTX

Download the MediaMTX executable from the official releases:

[MediaMTX Releases](https://github.com/bluenviron/mediamtx/releases)

## 2. Example Configuration

You can use the following HLS-related settings in your `mediamtx.yml` (or `mediamtx.example.yml`):

```yaml
# Number of HLS segments to keep. Increasing this uses more memory.
hlsSegmentCount: 7

# Duration of each HLS segment. Longer segments reduce CPU usage.
hlsSegmentDuration: 1500ms

# Duration of each HLS part (used in Low-Latency HLS).  
# Longer parts reduce CPU load and improve iOS compatibility.
hlsPartDuration: 500ms

# Automatically close the HLS muxer when there are no readers, freeing memory.
hlsMuxerCloseAfter: 30s

# Pull/publish the source only when at least one client is connected.
sourceOnDemand: yes

# Close the source when all clients disconnect, after this duration.
sourceOnDemandCloseAfter: 5s
