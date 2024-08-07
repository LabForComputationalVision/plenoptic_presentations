# Notes

Notes about presentations, largely done afterwards, focusing on how to improve
them.

## 2023-10-02

- the screen wasn't good, so many things were really small. try making sure they're larger
  - in particular, the noise initialization for the texture metamer (especially because the range was pretty tight)
- explain my model metamers slower (maybe focus on one model?)
- maybe don't use "identical", but "indistinguishable". or, be clearer that I mean "identical" to the model
- MAD competition:
  - step through the idea of the level slower, build it up
  - maybe tie back to metamers: there's a set of images / points that have identical distance. in this situation, we can plot them all out
  - L1 is less intuitive than L2
  - point out we know the level set like this because it's L1 and L2 -- in general, that's much harder to find, and so we rely on optimization
- geodesic:
  - analogy with plane paths across the globe might help make this easier to understand: if you look at the path of a flight from NYC to London on a flat map projection, it's confusing, looks very loopy. that's because it's a straight path along the sphere, etc
  - point out that VGG was designed to be shift-invariant (that's why it's convolutional) and its output is, but it clearly doesn't understand how objects move
  - add behavioral figure for VGG geodesics
- introduction needs more build up:
  - give motivation first, before introducing synthesis?
  - how to use plenoptic: come with models, it's a tool / framework for investigating them.
  - don't have to use our (or other Simoncelli-lab) models.
  - no learning happens on the models (which is majority of focus for machine learning, for example), all focus is on testing / evaluating
  - models must be stimulus-computable and written in pytorch
  - emphasize that plenoptic is *not* a model, the focus is not the modeling contents
  - need to show people how to integrate this with existing research. what are examples of how this can work
  - mention that this is all built on pytorch, takes advantage of their automatic differentiation, and largely done with iterative optimization

## 2023-10-23

- image space impossibly vast: for 256 x 256 black and white image (just 0 or 1) gives about 2^65000 possible images, and there are only 2^300 electrons in universe
- make connection to most-exciting stimuli work? (Tolias, Livingstone, etc). and point out that we're often interested in *invariances* as well (Tolias has recent paper looking at invariances)
- start with walking through that we have models that we want to compare to brains / behavior, and we need to know how to pick stimuli.
- problem with commonly chosen ones: standard artificial or natural images...
- plenoptic then contains methods to test specific model aspects: metamers test invariances, eigendistortions test sensitivities, etc. 
- metamers are global, eigendistortions local
- is it useful to draw a simple schematic of this? mapping between image space and representational space, showing there's a manifold in image space that corresponds to a single point in representational space, and we want to explore it somewhat. there are audiences for which that will be useful...

## 2024-07-16

- MAD Competition: use L1 vs L2 on map of Manhattan to introduce this idea (not just abstractly)
  - maybe also tie to "subway distance"
- in presentation for CSHL, people had a lot of clarifying questions around the slide where I showed the texture synthesis happening. probably still needs some build-up
