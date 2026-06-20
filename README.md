# Steam Manifest Hash Checker HTML

## Overview
The Steam Manifest Hash Checker is a simple, user-friendly tool that helps you verify your Steam game files. If you've ever wondered whether your game files are intact or need repair, this tool can help you check them against Steam's official data.

## Acknowledgments
- SteamKit2 code for reference implementation
- anadius for suggesting hash-wasm
- Masquerade for the original idea and testing

## AI Attribution Notice
This project was developed with partial assistance from Claude, an AI language model by Anthropic. The AI contributed to code optimization, implementation strategies, and documentation. The core functionality and original concept remain human-developed, with AI serving as a development aid for code refinement and feature implementation.

## Features
- Simple drag-and-drop interface
- Real-time checking progress
- Shows which files match, don't match, or are missing
- Multiple visual themes (Dark, Light, Blue, Steam, Synthwave, Ocean, Forest, Solarized)
- Folder visibility toggle
- Works with both Steam manifest files and SHA1 files
- Search function to find specific files
- Works directly in your browser - no installation needed
- Multi-Language support. No need to download the Languages
## How to Use
1. Open the tool in your web browser
2. Drop your Steam manifest or SHA1 file into the left drop zone
3. Drop the folder containing your game files into the right drop zone
4. Watch the progress as it checks your files
5. Review the results:
   - ✓ Green check: File is good
   - ⚠ Red warning: File needs attention
   - ⌛ Orange clock: Still checking
   - 📁 Blue folder: Folder entry

## Requirements
- A modern web browser (Chrome, Firefox, Edge, or Safari)
- Internet connection
- JavaScript enabled in your browser

## Browser Support
Works with:
- Chrome 80 or newer
- Firefox 80 or newer
- Edge 80 or newer
- Safari 14 or newer

## Future Improvements
Planned enhancements for the tool include:

### Under Development
- Nothing currently in active development

### Planned Features
- Batch Processing
  - Ability to check multiple folders at once
  - Queue system for large verifications
- Enhanced Reporting
  - Detailed verification reports
  - Export results to different formats
  - Statistics and analysis features
- User Experience
  - Customizable column layouts
  - More sorting and filtering options
  - Custom theme creation
  - Keyboard shortcuts

### Community Suggestions
We welcome feature suggestions from the community. Please submit your ideas through the issue tracking system.

## Technical Details
<details>
<summary>Click to show technical implementation details</summary>

### Implementation Features
- Using hash-wasm (v4.11.0) for fast SHA-1 computation
- 8MB chunk processing for efficient memory use
- Advanced path matching system
- Real-time progress tracking
- Supports multiple SHA1 file formats:
  - `<hash> *<filename>`
  - `SHA1(<filename>)= <hash>`
  - `<hash> <filename>`

### Architecture
- WebAssembly for hash calculations
- Protobuf parsing for Steam manifests
- Modular component design
- Score-based path matching
- Memory-efficient file processing
- Asynchronous operations

### Performance Optimizations
- Chunked file processing
- Throttled progress updates
- WebAssembly acceleration
- Optimized folder structure management
- Efficient path matching algorithms
</details>

## License
Available for personal use. Please check licensing for commercial applications.
