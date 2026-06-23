# Video to HLS Converter (Streamflix Tools)

A highly efficient utility designed to process, segment, and convert standard video files into HTTP Live Streaming (HLS) format (`.m3u8` playlists and `.ts` media segments). Optimized for adaptive bitrate streaming pipelines, this tool simplifies web video deployment and provides a seamless playback experience across multi-platform video players.

## 🚀 Features

- **Automated HLS Segmentation:** Dynamically splits video files into customizable target durations.
- **Adaptive Bitrate Ready:** Generates clear directory structures ideal for serving multi-resolution variants.
- **Cross-Platform Compatibility:** Output files are optimized for seamless integration with web players (like Video.js, HLS.js, or Plyr) as well as native iOS/Android players.
- **Optimized for Streaming:** Ensures proper keyframe alignment and stream segmenting to eliminate playback buffering and lag.

## 📋 Prerequisites

Before running the converter, ensure your environment meets the following requirements:

- **FFmpeg:** Ensure FFmpeg is installed on your system and added to your system's `PATH` environment variable. 
  - *To check if installed, run:* `ffmpeg -version`
- **Node.js / Python / Script Runtime:** (Adjust depending on whether your tool uses a Node.js, Python, or standard shell wrapper).

## 🛠️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/sudhanshugairola/VideotoHLS.git](https://github.com/sudhanshugairola/VideotoHLS.git)
   cd VideotoHLS
   ./videotohls -i input.mp4 -o output_folder/stream.m3u8
   or
   ffmpeg -i input.mp4 -codec: copy -start_number 0 -hls_time 10 -hls_list_size 0 -f hls output_folder/playlist.m3u8
