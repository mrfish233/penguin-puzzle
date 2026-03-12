# Penguin Puzzle — WebGL 3D Puzzle Game

Computer Graphics Final Project

A 3D puzzle game built from scratch with WebGL2 and GLSL shaders. Guide a penguin across blocks to reach the goal block.

## How to Play

Control the penguin to move from the **green** starting block to the **yellow** goal block.

| Input | Action |
|---|---|
| SPACE | Toggle first/third person view |
| W | Move forward (first person) |
| A / D | Turn left / right (first person) |
| Mouse | Rotate camera (third person) |
| Slider | Control mirror (Level 3) |

## Levels

- **Level 1** — Simple straight path
- **Level 2** — Rotating platform bridge
- **Level 3** — Mirror puzzle with slider-controlled reflective surface

## Graphics Features

- Phong lighting (ambient, diffuse, specular)
- Shadow mapping
- Skybox (cube-mapped environment)
- Dynamic cube-map reflections
- OBJ model loading (penguin)
- Procedural geometry (cube, sphere, cylinder)

## Running Locally

A local HTTP server is required (shader/model files use `fetch`).

```
python -m http.server 8080
```

Then open `http://localhost:8080` in a WebGL2-capable browser.

## Project Structure

```
├── index.html / level[1-3].html    Pages
├── src/
│   ├── webgl.js                    WebGL2 rendering engine
│   ├── shape.js                    Geometry primitives
│   ├── model.js                    OBJ parser
│   ├── controller.js               Input handling
│   ├── vertex-calc.js              Vertex/normal math
│   ├── cuon-matrix.js              Matrix library
│   └── shader/                     GLSL shaders (default, shadow, reflect, envcube)
├── levels/                         Level definitions
└── assets/                         Textures, penguin model, skybox
```
