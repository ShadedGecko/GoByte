# GoByte Font Format (GBFB & GBFA)

GoByte is a compact bitmap font format designed to store 8-bit, 16-bit, and 32-bit font data in a single file. It supports both basic and extended character sets, providing efficient encoding and quick access for applications with limited resources like embedded systems, games, or other graphical applications.

## File Formats

- **GBFB** (GoByte Font Basic): Stores fonts for 8-bit, 16-bit, and 32-bit sizes, supporting only the first 128 characters of the ASCII set (Basic Latin).
- **GBFA** (GoByte Font Advanced): Stores fonts for 8-bit, 16-bit, and 32-bit sizes, supporting the full 256-character extended ASCII set.

Both formats allow you to include multiple font sizes in a single file, optimizing for space and loading performance.

## Features

- **Compact**: Store 8-bit, 16-bit, and 32-bit fonts in a single file, reducing the overhead of multiple font files.
- **Optimized**: Designed for efficient encoding and small file sizes, making it ideal for memory-constrained environments.
- **Character Set Support**:
  - `GBFB`: Supports the first 128 characters (Basic Latin).
  - `GBFA`: Supports all 256 characters (Extended ASCII).
- **Cross-Platform**: Can be used across various programming languages and platforms, providing flexibility for different projects.

## Getting Started

To begin using the GoByte font format in your project, follow these instructions.

### 1. Installation

No external dependencies are required to use GoByte fonts. All you need is the `.GBFB` or `.GBFA` font files, which can be generated using the upcoming GoByte Font Generator tool.

### 2. Using GoByte Font Files

To load and use a GoByte font in your project:

1. **Load the font file**: Parse the `.GBFB` or `.GBFA` file in your application.
2. **Render the font**: Access the bitmap data for each character at the desired size (8-bit, 16-bit, or 32-bit) and render it on your screen or in your game.
3. **Text Rendering Options**: Choose the appropriate font size based on your needs (e.g., 8-bit for compact text or 32-bit for high-quality rendering).

### Example Code Snippet (Pseudocode)

```c
// Pseudocode for loading a GoByte Font file and rendering text

GoByteFont font;
LoadGoByteFont("myfont.GBFA", &font);  // Load the GBFA font file

// Render a character at 16-bit size
RenderCharacter(font, 'A', FONT_SIZE_16BIT);
