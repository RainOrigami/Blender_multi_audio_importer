# 🎧 Multi-Audio Importer — Blender Add-on

**Easily import all audio tracks from multi-track video files into Blender's Video Sequence Editor (VSE).**

Multi-Audio Importer is a powerful Blender addon that automatically detects, extracts, and imports all audio tracks from video files (such as multi-language movies, commentaries, or recordings with multiple microphones) directly into Blender's Video Sequence Editor as organized metastrips.

---

## ✨ Features

- **🔍 Smart Detection**: Automatically scans video files for all embedded audio tracks using FFprobe
- **🎯 Selective Import**: Choose which additional audio tracks to extract and import
- **📦 Metastrip Organization**: Groups original video with all audio tracks in a clean metastrip
- **⚡ Auto-Download**: Automatically downloads and installs static FFmpeg binaries (no manual installation required)
- **🛡️ Timeline Safety**: Preserves existing timeline content and original strip properties
- **📊 Progress Tracking**: Real-time progress updates with detailed logging
- **🎬 Format Support**: Works with `.mkv`, `.mp4`, `.mov`, `.avi`, and other container formats
- **🔧 Cross-Platform**: Supports Windows, macOS, and Linux

---

## 🛠 Requirements

- **Blender** 5.0+
- ffmpeg, ffprobe in PATH

---

## 📥 Installation

1. **Download** the addon file: [`multi_audio_importer.py`](multi_audio_importer.py)

2. **Open Blender** → Go to **Edit > Preferences > Add-ons**

3. **Click "Install..."** and select the downloaded `.py` file

4. **Enable** the addon by checking the box next to **"Multi-Audio Track Video Importer"**

---

## 🎬 How to Use

### Step 1: Prepare Your Video
1. Open the **Video Editing** workspace in Blender
2. Import your multi-track video file into the VSE timeline
3. **Disconnect the audio track from the video track** (Right-click the video strip → "Disconnect Strips")
4. **Select only the video strip** you want to process

> **⚠️ Important Notes:**
> - The addon **requires the audio to be disconnected from the video track** before processing
> - The addon **will not work when multiple strips are selected** - select only one video strip at a time
> - These instructions are so AI oh my god

### Step 2: Access the Multi-Audio Panel
1. In the **Side Panel** (press `N` if hidden), locate the **"Multi-Audio"** tab
2. The panel will show information about your selected video strip
3. Click **"Extract Additional Audio Tracks"**

### Step 3: Automatic Processing
The addon will automatically:
- Scan the video file for all audio tracks
- Extract additional audio tracks (beyond the first one)
- Create individual audio strips for each track
- Group everything except the original first strip into a clean metastrip
- Restore the original position and properties

### Step 4: Working with Results
- The resulting metastrip contains your original video plus all extracted audio tracks
- Enter the metastrip (Tab) to access individual audio tracks
- Each track is labeled with its title or track number
- All original timing, trimming, and effects are preserved

## ❓ Troubleshooting

### Common Issues

**"FFmpeg binaries not found"**
- Manually install FFmpeg and add it to your system PATH

**"No additional tracks found"**
- The video file may only contain one audio track
- Ensure you're using a video with multiple audio streams (common in MKV files)
- Try with a different video file to test functionality

**"Source file not found"**
- The video file path may be broken due to moving files
- Use Blender's "Make Paths Relative" feature
- Verify the source video file still exists at the expected location

**Steam Version of Blender**
- Steam installations may have path restrictions
- Consider using the standalone Blender version for better compatibility
- Manual FFmpeg installation may be required

### Debug Information
The addon provides detailed logging in Blender's Info panel and console:
- Audio track analysis results
- Extraction progress and timing
- File size and duration information
- Error details for troubleshooting

---

## 🤝 Contributing and 📄 License

The original project by https://github.com/MacArthurZZZ had no license, was taken by https://github.com/Jagard11 who removed the original author but fixed some stuff.  
I have added the original author again and further fixed some stuff.

---

## 👏 Credits

- **Author**: ~~Jagard11 & Claude AI~~ Yeah see, you can't just take other peoples projects and slap your name on it man. Original author is https://github.com/MacArthurZZZ with further edits by https://github.com/Jagard11 and https://github.com/RainOrigami
- **FFmpeg**: Uses the excellent FFmpeg project for audio processing
- **Community**: Thanks to the Blender community for feedback and testing

---

## 📬 Support

If you encounter issues or need help:  
Good luck!

**Enjoy seamless multi-track audio editing in Blender! 🎬🎵** 
