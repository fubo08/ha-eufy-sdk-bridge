# H.264 compatibility output

Set `TRANSCODE_H264` to a comma- or space-separated list of camera serials to convert their go2rtc output to H.264. The list is empty by default: unlisted cameras retain video copy. For a camera advertising several optical views, the setting applies to every advertised source while preserving each view's ID and URL query.

`TRANSCODE_WIDTH` defaults to 1280 pixels. Set it to 1920 for a larger compatibility output, or 0 to retain the incoming dimensions. Height follows the source aspect ratio and is rounded to an even number; a 2688Ã—1520 source therefore becomes 1920Ã—1086, not exactly 1920Ã—1080.

This performs a software encode while someone consumes the stream and uses additional CPU. It changes the bridge output only, not camera recording settings. It does not add audio; live audio is a separate feature.

Created with Codex.
