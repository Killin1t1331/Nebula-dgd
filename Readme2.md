https://killin1t1331.itch.io/nebula-digital-geometry-dynamics-engine

# Contextual Video Overlay Extension

A browser extension plugin that enhances video playback by injecting interactive, non-intrusive UI overlays. It surfaces contextual information, historical definitions (like the meaning of *Sophia*), and reference links dynamically based on video content or timestamps.

## Features

* **Collapsible Sidebar:** A slide-out panel for deep-dive resources that doesn't block the video player.
* **Hoverable Info Tooltips:** Minimalist icons overlaid on the video frame that reveal source links on hover/click.
* **Timestamp Sync:** Automatically surfaces relevant links matched to specific moments in the video timeline.
* **X-Ray Footer Mode:** A subtle, semi-transparent bottom bar displaying high-level metadata and quick links.

## Extension Architecture

The plugin maps contextual content to video playback using a structured data payload:

```json
{
  "timestamp": "02:15",
  "title": "Sophia in Ancient Cultures",
  "description": "Meaning 'wisdom' in ancient Greek, Sophia evolved from a philosophical virtue into a personified divine figure across Hellenistic, Jewish, and Gnostic traditions.",
  "links": [
    { "label": "Stanford Encyclopedia of Philosophy", "url": "https://stanford.edu" },
    { "label": "World History Encyclopedia", "url": "https://worldhistory.org" }
  ]
}
```

## Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com
   cd video-context-plugin
   ```

2. **Load the Extension in Your Browser:**
   * Open **Chrome** and navigate to `chrome://extensions/`.
   * Enable **Developer mode** (top-right toggle).
   * Click **Load unpacked** and select the root directory of this project.

3. **Usage:**
   * Navigate to any supported video streaming site.
   * The plugin will automatically detect the video player and mount the overlay UI components.

## UI Components

* `src/components/Sidebar/` - Handles the slide-out deep-dive panel.
* `src/components/Tooltip/` - Manages the hoverable info nodes pinned to the video frame.
* `src/components/Footer/` - Controls the persistent, minimal "Learn More" bottom bar.

## Contributing

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

## License

Distributed under the MIT License. See `LICENSE` for more information.
