# RimWorld Texture Optimizer

## Features

- **Universal Compatibility**: Works with any graphics card (NVIDIA, AMD, Intel Arc)
- **High Performance**: Processes 80,000+ textures in ~1 hour
- **Intelligent Upscaling**: Automatically upscales textures smaller than 256x256 to meet RimWorld standards
- **Background Operation**: No annoying popup windows, runs silently in background
- **Safe Backups**: Automatic backup system with easy restore functionality
- **Real-time Progress**: Live progress tracking with ETA display
- **Cancellation Support**: Stop conversion safely at any time
- **Standalone**: Single executable

## Requirements

- **Windows 10/11**
- **NVIDIA Texture Tools 3** installed in default location:
  ```
  C:\Program Files\NVIDIA Corporation\NVIDIA Texture Tools\nvcompress.exe
  ```
- **Free disk space** equal to your current texture size (for backups)

## Installation

### Option 1: Download Executable (Recommended)
1. Download `RimWorldOptimizer.exe` from [Releases](../../releases)
2. Place it anywhere on your computer
3. Run it directly - no setup required!

### Option 2: Build from Source
1. Download or clone this repository
2. Run `Start.bat` and choose option 2 to build the executable

## Quick Start

1. **Install NVIDIA Texture Tools 3** if you haven't already:
   - Download from [NVIDIA Developer](https://developer.nvidia.com/texture-tools-exporter)
   - Install to the default location

2. **Run RimWorldOptimizer.exe**

3. **Select your RimWorld Mods folder** (usually `C:\Steam\steamapps\common\RimWorld\Mods`)

4. **Click "Start Conversion"** and minimize the window

5. **Wait for completion** - progress is shown in the window title

## Important Notes

- **Backup your mods** before first use (recommended but not required - tool creates its own backups)
- **Conversion modifies your mod files** - original PNGs are saved as `.png-backup`
- **Use "Restore" function** to undo all changes if needed
- **Test your game** after conversion to ensure everything works properly

## What It Does

### Before Conversion:
```
texture.png          (original file)
```

### After Conversion:
```
texture.dds          (optimized texture)
texture.png-backup   (original backup)
```

### Performance Benefits:
- **Faster loading times** - especially during mod loading
- **Reduced VRAM usage** - DDS is more GPU-friendly
- **Smaller file sizes** - typically 40-60% size reduction
- **Same visual quality** - lossless conversion for most textures
- **Automatic upscaling** - ensures all textures meet RimWorld's 256x256 minimum standard
- **Maintained aspect ratios** - upscaling preserves original proportions

## Advanced Usage

For power users, the repository includes:
- **CLI version** (`rimworld_texture_optimizer.py`) with command-line interface
- **Batch automation** via `Start.bat` with multiple options
- **Configuration file** support for custom paths

## Troubleshooting

### "nvcompress.exe not found"
- Install NVIDIA Texture Tools 3 to the default location
- Verify the file exists at: `C:\Program Files\NVIDIA Corporation\NVIDIA Texture Tools\nvcompress.exe`

### "No PNG files found"
- Verify your RimWorld Mods folder path is correct
- Ensure you have mods installed

### Conversion errors
- Check that you have write permissions to your mods folder
- Ensure sufficient free disk space for backups
- Try running as administrator if permission issues persist

## Performance Comparison

| Tool | Hardware | 80k+ Files | Notes |
|------|----------|------------|-------|
| **RimWorld Optimizer** | Any GPU | ~1 hour | Universal compatibility |
| RimPy (GPU) | NVIDIA only | ~2-4 hours | CUDA required |
| RimPy (CPU) | Any | 12+ hours | Fallback mode |

## Contributing

This tool was built to solve Intel Arc B580 compatibility issues with existing texture converters, but benefits all users with its speed and simplicity.

## License

CC0

---

Made with love for the RimWorld modding community
