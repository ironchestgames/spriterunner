*I was doing animations in sketch and wanted to see the results fairly fast. Use at your own risk. <3*

## Usage

http://localhost:8000/spriterunner.html?file=out.png&amp;height=128

The idea is to change your image and then reload.

Will save to localStorage:
- if flipped horizontally and/or vertically
- the current frame
- the current interval time

arguments:
- file=[filepath]
- height=[frame height in pixels]

optional:
- width=[frame width in pixels, default to height]
- bgcolor=[format: rrggbb (like hex), defaults to browser default]

## Bonus

Use imagemagick montage with fswatch to automatically create the spritesheet from separate images, like so:
fswatch -0 -o . | xargs -0 -n 1 -I {} montage -background none -geometry +0+0 my_animation_* out.png

Use symbolic link to your file instead of putting it in the correct path for spriterunner/your serving solution.
