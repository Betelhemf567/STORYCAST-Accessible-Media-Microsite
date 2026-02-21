# Media Asset Placeholders

This file explains the placeholder media assets for the StoryCast project.

## Video File (video.mp4)
**Purpose:** Main video player content for story pages
**Location:** assets/video.mp4
**Note:** This is a placeholder. In production, replace with actual video content.

**Requirements for production video:**
- Format: MP4 (H.264 codec)
- Resolution: 1920x1080 or higher
- Frame rate: 30fps
- Audio: AAC, 48kHz
- Include closed captions (VTT format provided in assets/captions-en.vtt)
- Include audio descriptions track (VTT format provided in assets/descriptions-en.vtt)

## Audio File (audio.mp3)
**Purpose:** Audio-only version for podcast listening
**Location:** assets/audio.mp3
**Note:** This is a placeholder. In production, replace with actual audio content.

**Requirements for production audio:**
- Format: MP3 or OGG
- Bitrate: 128kbps or higher
- Sample rate: 44.1kHz or 48kHz
- Mono or stereo
- Normalized audio levels

## Caption Files
- **captions-en.vtt**: English captions for video content (WCAG AA compliant)
- **descriptions-en.vtt**: Audio descriptions for visually impaired users

## Transcript
- **transcript.txt**: Full text transcript of the story content

## For Development/Testing
You can use these placeholder URLs for testing:
- Sample video: https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4
- Sample audio: Any royalty-free audio file

## Accessibility Notes
All media must include:
1. Captions/subtitles (VTT format)
2. Full text transcript (downloadable)
3. Audio descriptions (for video content)
4. Keyboard-accessible controls
5. Proper ARIA labels

This ensures WCAG 2.1 AA compliance for all users.
