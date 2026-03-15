# Martini

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

Martini is an experimental JavaScript library for real-time terrain mesh generation from height data.

## Demo
See the algorithm in action and read more about how it works in [this interactive Observable notebook](https://observablehq.com/@mourner/martin-real-time-rtin-terrain-mesh).

## Features
- Generates a hierarchy of triangular meshes of varying level of detail in milliseconds
- Based on the "Right-Triangulated Irregular Networks" algorithm

## Usage

### Install
```bash
npm install @mapbox/martini
```

### Example
```js
// set up mesh generator for a certain 2^k+1 grid size
const martini = new Martini(257);

// generate RTIN hierarchy from terrain data (an array of size^2 length)
const tile = martini.createTile(terrain);

// get a mesh (vertices and triangles indices) for a 10m error
const mesh = tile.getMesh(10);
```

## Ports to other languages
- [pymartini](https://github.com/kylebarron/pymartini) (Python)

## License
ISC