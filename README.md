<div style="text-align: center; transform: scale(.5);">
  <img src="card-repo.png"/>
</div>

# @tldraw/intersect

This package contains 2D intersection utility functions used by [tldraw](https://tldraw.com).

💕 Love this library? Consider [becoming a sponsor](https://github.com/sponsors/steveruizok?frequency=recurring&sponsor=steveruizok).

## Installation

Use your package manager of choice to install `@tldraw/intersect`.

```bash
yarn add @tldraw/intersect
# or
npm i @tldraw/intersect
```

## Usage

This library exports many intersection functions. You can use these methods to find intersection points between various 2D shapes. Points are formatted as `[x, y]`.

```tsx
import { intersectLineSegmentEllipse } from "@tldraw/intersect"

const A = [5, 5]
const B = [10, 10]
const ellipse = { center: [10, 10], rx: 5, ry: 4, rotation: Math.PI / 6 }

const intersections = intersectLineSegmentEllipse(
  A,
  B,
  ellipse.center,
  ellipse.rx,
  ellipse.ry,
  ellipse.rotation
)
```

An intersection is formatted as:

```ts
export type TLIntersection = {
  didIntersect: boolean
  message: string
  points: number[][]
}
```

Some intersection functions, such as `intersectLineSegmentLineSegment`, will return a single intersection. Others, such as `intersectRectangleRectangle`, will return an array of several intersections.

## Community

### Support

Need help? Please [open an issue](https://github.com/tldraw/intersect/issues/new) for support.

### Discussion

Want to connect with other devs? Visit the [Discord channel](https://discord.gg/s4FXZ6fppJ).

### License

This project is licensed under MIT. If you're using the library in a commercial product, please consider [becoming a sponsor](https://github.com/sponsors/steveruizok?frequency=recurring&sponsor=steveruizok).

## Author

- [@steveruizok](https://twitter.com/steveruizok)
