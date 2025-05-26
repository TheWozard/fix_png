# fix_png
While working with [Inkscape](https://inkscape.org/) and [Bevy](https://bevyengine.org/), it was found that the default flat transparent background color was used during sampling when drawing images.

One option is to disable linear sampling in Bevy with:
```rust
app.add_plugins(DefaultPlugins.set(ImagePlugin::default_nearest()))
```
But this makes edges hard and removes smoothing caused by linear sampling.

This repo solves the issue by updating the transparent pixels to match the color of their neighbors.

## Usage
Will only update PNG files regardless of glob.

```
fix_png --glob "./images/*"
```

## Example
The following is an example of the issue. The intended outcome is to have a purely black diamond.

<div style="display: flex">
    <img src="docs/issue.png"/>
    <img src="docs/fixed.png"/>
</div>
