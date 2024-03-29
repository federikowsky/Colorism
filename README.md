# Colorism

## Overview

This Python library provides a convenient way to work with ANSI color codes for text and background styling. The library includes classes for text and background styles, a different color palettes, and various color conversion methods. It has a very simple, fast, light and has intuitive syntax.

Provides also a `Converter` which contain a set of methods for converting between different color representations. The class supports conversions between RGB, hexadecimal, HSL (Hue, Saturation, Lightness), and HSV (Hue, Saturation, Value) color formats.

### Key Features:

- **Text and Background Styles:** The library provides classes for both text and background styles, allowing users to effortlessly enhance the visual presentation of text content.

- **Support for 8-bit and 24-bit Colors:** The library supports both 8-bit and 24-bit colors, allowing users to choose the color depth that best suits their needs.

- **Color Palettes:** Explore various color palettes, including standard and intense colors, grayscale, and rainbow palettes, providing flexibility for diverse styling needs.

- **Color Conversion:** The `Converter` class makes it easy to switch between different color formats. Users can effortlessly convert colors from RGB, hexadecimal, HSL (Hue, Saturation, Lightness), to HSV (Hue, Saturation, Value).

## Usage

```python
from colorism import FG, BG

print(FG.RED + "Hello World" + FG.RESET)
print(BG.RED + "Hello World" + BG.RESET)
```

```python
from colorism import FG, BG

print(FG.bold("Hello World"))
print(FG.dim("Hello World"))
```

### Advanced Usage
```python
from colorism import FG, BG

print(f"{FG.RED + BG.YELLOW}Hello World {FG.RESET + BG.RESET}")
print(f"{FG.BOLD + FG.UNDERLINE + FG.GREEN + BG.rgb2escape(0, 255, 255)} Hello World. {FG.RESET_ALL}")
```

```python
from colorism import FG, BG

print(f"{FG.hsl2escape(60, 100, 25) + BG.rgb2escape(255, 255, 255)}Hello World {FG.RESET + BG.RESET}")
```

## License
This project is distributed under the MIT License. See the [LICENSE](LICENSE) file for more details.
