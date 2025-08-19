# ATC Radio Effect

A real-time audio processing web application that applies Air Traffic Control (ATC) radio effects to live audio streams.

## Features

- **Live Stream Processing**: Connect to any live audio stream URL (MP3/audio streams)
- **ATC Radio Effect**: Simulates the characteristic sound of air traffic control radio communications
- **Real-time Controls**: Adjustable effect intensity and toggle on/off
- **Audio Processing Chain**: 
  - Band-pass filtering (200-3400 Hz range)
  - Dynamic compression/AGC
  - Soft clipping distortion
  - Optional bit crushing
  - Background noise with envelope-following ducking
  - Squelch tail effects

## Usage

1. Open `index.html` in a modern web browser
2. Enter a live audio stream URL in the "Stream URL" field
3. Click "Load" to connect to the stream
4. Click "Play" to start playback with ATC effects applied
5. Use the "Effect On" checkbox to toggle processing
6. Adjust "Intensity" slider to control the strength of the radio effect

## Technical Details

- Uses Web Audio API for real-time audio processing
- Implements AudioWorklet for custom bit crushing effects
- Features envelope-following noise ducking for realistic radio behavior
- Includes squelch tail simulation with brief noise bursts
- Cross-origin audio support for external streams

## Browser Compatibility

Requires a modern browser with Web Audio API support (Chrome, Firefox, Safari, Edge).

## Note

Ensure audio streams support CORS for cross-origin access, or serve from the same domain.