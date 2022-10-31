# Rust Graphics Crates
This is an opinionated list of modern graphics crates in Rust. I noticed it was really hard to keep track of all the good graphics crates going around, so I made this to help me and others. The categories are more based on grouping crates with similar levels of abstraction and less to do with the category name itself. I'm happy to take PRs, but I want to make sure all the crates on the list are actively maintained and have promise.

Although a bit outdated, [icefoxen](https://github.com/icefoxen), author of ggez, wrote a great article about the current state of graphics crates back in May of 2019. A lot of what's said is still applicable today and can be found [here]( https://wiki.alopex.li/AGuideToRustGraphicsLibraries2019).

## Game Frameworks
Although they consider themselves "game frameworks," they can, of course, be used as a general graphics engine.
- [ggez](https://github.com/ggez/ggez) ![Crates.io (recent)](https://img.shields.io/crates/dr/ggez)
  - **Backend**: gfx (not gfx-hal)
    - OpenGL 2.1+
    - OpenGL ES2+ (works on Android as well as WebGL2)
    - Direct3D 11
- [bevy](https://github.com/bevyengine/bevy) ![Crates.io (recent)](https://img.shields.io/crates/dr/bevy) 
  - **Backends**:
    - wgpu
    - WebGL

## High-Level
These should allow you to render something with relative ease. 
- [piet](https://github.com/linebender/piet) ![Crates.io (recent)](https://img.shields.io/crates/dr/piet)
  - **Custom Backend With Support For**:
    - Cairo
    - Core Graphics
    - Direct2D
    - Web
- [macroquad](https://github.com/not-fl3/macroquad) ![Crates.io (recent)](https://img.shields.io/crates/dr/macroquad)
  - **Backend**: miniquad
- [pathfinder](https://github.com/servo/pathfinder) ![Crates.io (recent)](https://img.shields.io/crates/dr/pathfinder)
  - **Custom Backend With Support For**:
    - OpenGL 3
    - OpenGL ES 3
    - WebGL 2
    - Metal
- [skulpin](https://github.com/aclysma/skulpin) ![Crates.io (recent)](https://img.shields.io/crates/dr/skulpin)
  - **Backend**: Skia + Vulkan

## Simple
These crates provide a simple framebuffer.
- [softbuffer](https://github.com/john01dav/softbuffer) ![Crates.io (recent)](https://img.shields.io/crates/dr/softbuffer)
  - **Put a user-created 2D buffer on a window without relying on GPU infrastructure (like minifb but integrates with raw-window-handle to work with winit and other standard window management libraries)**
- [pixels](https://github.com/parasyte/pixels) ![Crates.io (recent)](https://img.shields.io/crates/dr/pixels)
  - **Backend**: wgpu
- [minifb](https://github.com/emoon/minifb) ![Crates.io (recent)](https://img.shields.io/crates/dr/minifb)
  - **Put a user-created 2D buffer on a window without relying on GPU infrastructure (does own window management)**

## Low-Level
These will give you a lot of control over how rendering is done, but will take a lot more work/code than a higher-level crate
- [wgpu](https://github.com/gfx-rs/wgpu-rs) ![Crates.io (recent)](https://img.shields.io/crates/dr/wgpu)
  - **Backends**:
    - gfx-hal (including WebGL)
    - WebGPU
- [miniquad](https://github.com/not-fl3/miniquad) ![Crates.io (recent)](https://img.shields.io/crates/dr/miniquad)
  - **Custom Backend With Support For**:
    - OpenGL 3
    - OpenGL ES 3
    - WebGL 1
- [gfx-hal](https://github.com/gfx-rs/gfx) ![Crates.io (recent)](https://img.shields.io/crates/dr/gfx-hal)
  - **Backends**:
    - Vulkan (via `ash`)
    - Direct3D 12
    - Direct3D 11
    - Metal (via `metal`)
    - OpenGL ES-3 (via `glow`)
    - WebGL (via `glow`)
- [vulkano](https://github.com/vulkano-rs/vulkano) ![Crates.io (recent)](https://img.shields.io/crates/dr/vulkano)
  - **Backend**: Vulkan
- [rust-sdl2](https://github.com/Rust-SDL2/rust-sdl2) ![Crates.io (recent)](https://img.shields.io/crates/dr/sdl2)
  - **Backend**: SDL2
- [ash](https://github.com/MaikKlein/ash) ![Crates.io (recent)](https://img.shields.io/crates/dr/ash)
  - **Backend**: Vulkan
- [metal](https://github.com/gfx-rs/metal-rs) ![Crates.io (recent)](https://img.shields.io/crates/dr/metal)
  - **Backend**: Metal
- [glow](https://github.com/grovesNL/glow) ![Crates.io (recent)](https://img.shields.io/crates/dr/glow)
  - **Backends**:
    - OpenGL
    - OpenGL ES
    - WebGL
