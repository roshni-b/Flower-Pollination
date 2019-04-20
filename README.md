# Flower Pollination Algorithm Implementation
Flower pollination algorithm is a metaheuristic algorithm that was developed by [Xin-She Yang](https://en.wikipedia.org/wiki/Xin-She_Yang), based on the pollination process of flowering plants.

## Usage:

##### 1. Cloning the repository.
```
git clone https://github.com/roshni-b/Flower-Pollination.git
cd Flower-Pollination
```

##### 2. Running the [script](https://github.com/roshni-b/Flower-Pollination/blob/master/fpa_demo.m) in MATLAB
```
fpa_demo.m
```
## Assumptions
1. Biotic and cross-pollination is considered as a global pollination process with pollen carrying pollinators performing Levy flights.
2. Abiotic and self-pollination are considered as local pollination.
3. Flower constancy can be considered as the reproduction probability is proportional to the similarity of two flowers involved.
4. Local and global pollination are controlled by a switch probability in [0,1] . Due to the physical proximity and other factors such as wind, local pollination can have a significant fraction q in the overall pollination activities.

## Pseudo-code 
![alt text](https://github.com/roshni-b/Flower-Pollination/blob/master/pseudocode_fpa.png "psudo-code")

### Citation
> Xin-She Yang, Flower pollination algorithm for global optimization, in: Unconventional Computation and Natural Computation 2012, Lecture Notes in Computer Science, Vol. 7445, pp. 240-249 (2012).
