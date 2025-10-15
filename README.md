# Mouse Accuracy Tester

A web-based mouse accuracy testing application that measures precision and reaction time with pixel-perfect accuracy tracking.

## Features

### 🎯 Precision Testing
- **Pixel-Perfect Accuracy**: Uses Chebyshev distance calculation for discrete pixel ring measurements
- **Progressive Difficulty**: Targets decrease in size throughout the test
- **Real-time Statistics**: Track accuracy percentage and response time for each click

### 🎮 Multiple Difficulty Modes

**Easy Mode** (41px - 17px targets)
- 5×5 pixel perfect accuracy zone (25 pixels)
- Ideal for beginners or casual testing

**Medium Mode** (29px - 11px targets)
- 3×3 pixel perfect accuracy zone (9 pixels)
- Balanced challenge for intermediate users

**Hard Mode** (15px - 3px targets)
- Exact center pixel only (1×1 perfect zone)
- Ultimate precision challenge

### 📐 Resolution Options
Choose from 8 different screen resolutions or fullscreen mode:
- Fullscreen (adaptive to your display)
- 3840×2160 (4K UHD)
- 2560×1440 (QHD)
- 2048×1152
- 1920×1080 (Full HD)
- 1536×864
- 1440×900
- 1366×768

The test area is visually constrained and centered when using specific resolutions, with automatic validation if selected resolution exceeds your screen size.

### 📊 Comprehensive Results

After completing the test, view detailed statistics including:
- Overall average accuracy and response time
- Per-size group statistics
- Individual click data with accuracy, response time, and pixel distance
- Difficulty mode and resolution information

## Screenshots

### Start Screen
Configure your test with resolution and difficulty selection:

![Start Screen](images/accuracy%20test%20settings.png)

### Test In Progress
Click on the center pixel of each progressively smaller target:

![Test In Progress](images/Accuracy%20test%20in%20progress.png)

## How It Works

### Accuracy Calculation

The application uses **Chebyshev distance** (maximum of X and Y pixel differences) to create discrete "rings" around the center pixel. This provides more intuitive accuracy measurements than Euclidean distance.

**Difficulty-Based Perfect Zones:**
- Clicks within the perfect zone receive 100% accuracy
- Beyond the perfect zone, accuracy decays linearly to 0% at the target edge
- Different difficulties have different perfect zone sizes, making them progressively more challenging

### Test Flow

1. **Select Resolution**: Choose your preferred test area size
2. **Select Difficulty**: Pick Easy, Medium, or Hard mode
3. **Countdown**: 5-second countdown with audio beep
4. **Testing**: Click 16 targets (4 sizes × 4 rounds each)
   - Audio beep signals transitions to smaller target sizes
5. **Results**: Review comprehensive statistics and accuracy metrics

## Getting Started

### Running Locally

Simply open `index.html` in any modern web browser:

```bash
open index.html
```

Or visit the live demo: [Mouse Accuracy Tester](https://crypto69.github.io/mouse-accuracy-tester/)

### Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- Fullscreen API support (optional, but recommended for best experience)

## Technical Details

### Architecture
- **Single-file application**: All HTML, CSS, and JavaScript in one file
- **No dependencies**: Pure vanilla JavaScript
- **Responsive design**: Adapts to different screen sizes with scrolling support

### Key Features
- Pixel-perfect center calculation using odd-numbered dimensions
- Coordinate system conversion for accurate positioning
- Web Audio API for countdown and transition beeps
- Fullscreen API integration for immersive testing

## Use Cases

- **Gamers**: Test and improve mouse precision for FPS and competitive gaming
- **Designers**: Verify pixel-accurate cursor control for detailed work
- **Hardware Testing**: Compare different mice, mousepads, or DPI settings
- **Benchmarking**: Track improvement over time with consistent metrics
- **Accessibility**: Test mouse control for accessibility evaluations

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

---


