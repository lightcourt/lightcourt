# Lightcourt

**Shared, access-controlled camera views for interactive live streaming.**

Lightcourt is a planned open-source, self-hosted service that keeps cameras on a private network, turns each camera into named views (crops, rotations, splits) and delivers only authorised views to other applications, as refreshing JPEG, MJPEG or low-latency WebRTC, with explicit image-freshness status.

The name comes from the light court of a building: one shared source of light, seen by each room through its own window.

Lightcourt is the successor of [WILSP](https://github.com/zstars/wilsp), the interactive live-streaming platform published in 2017 with the IEEE Access paper *An Open and Scalable Web-Based Interactive Live-Streaming Architecture: The WILSP Platform* ([doi:10.1109/ACCESS.2017.2710328](https://doi.org/10.1109/ACCESS.2017.2710328)), which streams LabsLand's real-time remote laboratories.

## Planned design

- One camera, many views, each with its own identity, permission and freshness state.
- Three serving modes per view: refreshing JPEG, MJPEG and WebRTC (WHIP/WHEP where available).
- Cameras are never exposed: viewers receive authorised views, never camera credentials or web interfaces.
- Host applications issue short-lived per-view tokens; Lightcourt stores no end users.
- Builds on FFmpeg and existing open media engines through a replaceable adapter.
- A single Go binary for x86_64 and ARM64, with an API, a management panel and an embeddable web component.

## Status

Design phase. Code, documentation and tests will be developed in this repository.

## Licence

Code: Apache-2.0. Documentation: CC BY 4.0.

Maintained by [LabsLand](https://labsland.com).
