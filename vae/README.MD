The Blank Slate: We start with an empty 
8
×
8
8×8
 grid.
PixelCNN Generates (The "Rough Draft"):
Pixel (0,0): PixelCNN says: "There is a 60% chance this should be Code 12 (Blue Sky)." We roll a dice. We pick 12.
Pixel (0,1): "Given that the left neighbor is 12... there is a 90% chance this is also 12." We pick 12.
... (Repeat 64 times) ...
Pixel (4,4): "Given the surroundings, this should be Code 88 (Beak)."
Result: We have a completed 
8
×
8
8×8

 grid of Indices.
Codebook Lookup:
We swap Index 12 for Vector #12.
We swap Index 88 for Vector #88.
Result: We have an 
8
×
8
8×8
 grid of Vectors.
Decoder Upsampling (The "Final Polish"):
The Decoder runs its Transposed Convolutions over the grid.
It sees Vector #12 next to Vector #88.
It uses its learned weights to blend the transition.
It expands the 8x8 grid into 32x32 pixels.
Final Result: A high-resolution image of a bird, with smooth gradients and sharp edges, generated from scratch.