## Mandlebrot sets

[Link][link]

[link]: https://pv97.github.io/Mandlebrot/

### Background

The core series being investigated is is z_n+1 = z_n^2 + c where z and c are complex numbers.
The graph displayed lies on the complex plane of a+bi, which represents the values of c choosen for the series.
We are interested in how fast the series z_n diverges with chosen initial z_0 and c, so we color the
graph with white representing no divergence and black representing rapid divergence.

The default set being displayed is the Mandelbrot set, where z_0 is set to be 0. Thus the Mandlebrot set is a 2D
representation of a 3D fractal surface.

A related collection of sets are the Julia sets, of which is generated by instead testing the covergence of a fixed c, with
varying z values from the complex plane. Thus the Mandlebrot set is the intersection at the origin on the complex plane with
the Julia sets following the series z_n+1 = z_n^2 + c.

To truly appeciate the duality of these two sets, this tool is created to explore the various Mandlebrot sets for different
initial z values, allowing, albeit gradual, exploration of the 5D fractal surface of the divergence of this beautiful series.
### Functionality & MVP  

With this Julia/Mandlebrot set generator, users will be able to:

- [ ] Choose initial values for z
- [ ] Zoom into the Mandlebrot sets

### Wireframes

This app will consist of a graph with an settings box. Users will be able to choose the z values in this box. Users can drag a rectangle on the graph to choose a zoom area.

![wireframes](wireframe.png)

### Architecture and Technologies

This project will be implemented with the following technologies:

- Vanilla JavaScript and `jquery` for overall structure and game logic,
- `HTML5 Canvas` for DOM manipulation and rendering,
- Webpack to bundle and serve up the various scripts.

In addition to the webpack entry file, there will be four scripts involved in this project:

`graph.js`: this script will handle the logic for drawing the Mandlebrot sets.

`Jgraph.js`: this script will handle the logic for drawing the Julia sets.

`rectangle.js`: this script will handle drawing zoom rectangles.

`complex.js`: this script will handle complex numbers.

`util.js`: this script will handle screen recalculation.

`mandlebrot.js`: this script will handle user inputs and calls graph to render.

### Implementation Timeline

**Day 1**: Setup all necessary Node modules, including getting webpack up and running and `Easel.js` installed.  Create `webpack.config.js`.  Write a basic entry file and the bare bones of all 3 scripts outlined above. Goals for the day:

- Get a green bundle with `webpack`
- Set up `graph.js` to render individual pixels

**Day 2**: Produce a non-interactable Mandlebrot set by implementing the z^2+c algorithm for z = 0.  Goals for the day:

- Render Mandlebrot set

**Day 3**: Work on `mandlebrot.js` to create the settings box to allow users to change z inputs.  Goals for the day:

- create settings box
- inputs change graph render

**Day 4**: Add listeners to mouse click to implement zoom rectangles.  Goals for the day:

- Add zoom function to graph
- Zoom updates graph params to graph and triggers render


### Bonus features

- [ ] Add options for different different color schemes
- [ ] Add slice rotation
