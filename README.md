# Loupe

Finds the sharpest frames in a video and lets you save them as images. Runs entirely in the browser — no upload, no server.

## How it works

1. Drop in a video file.
2. Loupe samples a frame every X seconds (you set the interval).
3. Each frame gets scored for sharpness and exposure.
4. The best frames are kept and shown on a timeline and in a grid, sortable by time or score.
5. Open any frame in the viewer to zoom, pan, and save it as JPEG.

## Features

- Works with mp4, webm, mov, mkv
- Hardware-accelerated decoding, with a seek-based fallback if that's not available
- Own WebM parser — no external library needed for that format
- Adjustable sample interval and number of frames to keep
- Optional refine step: re-checks around the best moments for a sharper frame
- Sharpness timeline for the whole clip
- Dark and light theme
- Frame viewer with zoom, pan, and one-click save

## Use

Download `loupe.html` and open it in a browser. No install, no build step, works offline.

## Notes

- The video is processed in your browser tab and never leaves your machine.
- Sharpness is scored using local contrast, combined with an exposure check, so it favors frames that are both sharp and well-lit.
- Large files are read in chunks; past a size cap, Loupe falls back to a slower, lower-memory decode path.

## License

MIT — see [LICENSE](LICENSE).
