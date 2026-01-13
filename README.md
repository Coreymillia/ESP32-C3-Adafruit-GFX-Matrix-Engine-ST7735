# ESP32-C3 Matrix Engine - ST7735 Edition

A Matrix-style screensaver with 113 effects and 22 fonts, ported to ESP32-C3 SuperMini with 1.77" ST7735 TFT display.
Making 2,486 variations
## Hardware

- **ESP32-C3 SuperMini** (160MHz RISC-V, 320KB RAM, 4MB Flash)
- **1.77" ST7735 TFT** (160x128 pixels, landscape orientation)
- **Dual button control** (boot button + external button)

### Wiring
```
ESP32-C3 SuperMini → ST7735 Display
GPIO 4  (SCK)  → SCL/SCK
GPIO 6  (MOSI) → SDA/MOSI  
GPIO 10 (CS)   → CS
GPIO 7  (DC)   → DC/RS
GPIO 2  (RST)  → RES/RST
3.3V           → VCC
GND            → GND

Optional:
GPIO 3  → External Button (to GND)
GPIO 9  → Boot Button (built-in)
```

## Features

### 113 Matrix Effects
The code implements exactly **113 matrix rain variations** including:

**Basic Matrix (20 effects)**
- MATRIX_CUSTOM - Custom matrix rain
- MATRIX_XSCREEN - Xscreensaver authentic matrix  
- BINARY_RAIN - Binary code (0s and 1s)
- GLMATRIX_3D - GLMatrix-inspired 3D effect
- MATRIX_MULTICOLOR - Multi-colored rain
- MATRIX_SPEEDBURST - Speed burst columns
- MATRIX_NEONGREEN - Neon green gradient
- MATRIX_PULSE - Pulsing brightness
- MATRIX_GLITCH - Glitchy flickers
- MATRIX_BROKEN - Broken streams with pauses
- MATRIX_RETRO - Retro amber terminal
- MATRIX_FIRE - Fire colors (red/orange/yellow)
- MATRIX_ICE - Ice colors (blue/white/cyan)
- MATRIX_TOXIC - Toxic green/yellow
- MATRIX_CYBER - Cyberpunk purple/pink
- MATRIX_STORM - Lightning white/blue/purple
- MATRIX_BLOOD - Dark red dripping
- MATRIX_GOLD - Golden yellow/amber
- MATRIX_VOID - Inverted colors
- MATRIX_PHANTOM - Ghost trails

**Advanced Effects (60+ more)**
- Wind effects (MATRIX_WIND, MATRIX_WINDSTORM, MATRIX_HEAVYWIND)
- Ripple effects (MATRIX_RIPPLE, MATRIX_TIDAL, MATRIX_SLOWRIPPLE) 
- Drip physics (MATRIX_DRIP_BLOOD, MATRIX_DRIP_HONEY, MATRIX_DRIP_ACID)
- Fracture patterns (MATRIX_FRACTURE_BINARY, MATRIX_FRACTURE_EXPLOSIVE)
- Advanced physics (MATRIX_MOLTEN, MATRIX_GRAVITYWELL, MATRIX_RESONANCE)

**Font Variations (30+ effects)**
- MATRIX_MICROFONT family - Ultra-dense tiny characters
- MATRIX_BIGFONT - Large chunky characters  
- Font selector modes with different typefaces

### 22 Fonts with Auto-Cycling
- **Original 12 fonts**: FreeSans, FreeMono, FreeSerif in various sizes
- **10 NEW fonts added**: Picopixel, Org_01, italic variations, bold italic combinations
- **Auto font cycling**: Changes after mode 107

### Controls
- **Boot Button (GPIO 9)**: Cycle through all 113 effects
- **External Button (GPIO 3)**: Additional control
- **Auto-advance**: Enabled by default, switches effects every 30 seconds
- **Long press**: Toggle auto-advance ON/OFF with visual feedback

## Installation

### Requirements
- PlatformIO installed
- USB-C cable

### Build & Upload
```bash
pio run --target upload
```

### Libraries Used
- Adafruit_GFX_Library @ 1.12.4
- Adafruit_ST7735_and_ST7789_Library @ 1.11.0

## Performance
- **RAM Usage**: 12.3% (40,160 / 327,680 bytes)
- **Flash Usage**: 35.1% (460,112 / 1,310,720 bytes) 
- **Smooth animation** at 60+ FPS
- **8000+ lines of code** in main.cpp

## What This Actually Is

This is a **matrix screensaver** - it displays cascading digital rain effects like in the movie "The Matrix". All 113 effects are variations of matrix rain with different:
- Colors (fire, ice, toxic, cyberpunk themes)
- Physics (wind sway, ripples, dripping, fractures)
- Typography (22 different fonts and sizes)
- Behaviors (pulsing, glitching, ghosting, gravity effects)

No other screensaver types - just matrix rain perfected with 113 variations.

## Version History
- **v2.0** (Jan 13, 2026): Added 10 new fonts (12→22 total)
- **v1.0** (Jan 12, 2026): 113 matrix effects, 12 fonts

---
*A hypnotic matrix screensaver for your ESP32-C3* ✨
