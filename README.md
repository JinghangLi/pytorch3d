<img src="https://raw.githubusercontent.com/facebookresearch/pytorch3d/master/.github/pytorch3dlogo.png" width="900"/>

[![CircleCI](https://circleci.com/gh/facebookresearch/pytorch3d.svg?style=svg)](https://circleci.com/gh/facebookresearch/pytorch3d)
[![Anaconda-Server Badge](https://anaconda.org/pytorch3d/pytorch3d/badges/version.svg)](https://anaconda.org/pytorch3d/pytorch3d)

# Introduction

PyTorch3D provides efficient, reusable components for 3D Computer Vision research with [PyTorch](https://pytorch.org).

Key features include:

- Data structure for storing and manipulating triangle meshes
- Efficient operations on triangle meshes (projective transformations, graph convolution, sampling, loss functions)
- A differentiable mesh renderer

PyTorch3D is designed to integrate smoothly with deep learning methods for predicting and manipulating 3D data.
For this reason, all operators in PyTorch3D:

- Are implemented using PyTorch tensors
- Can handle minibatches of hetereogenous data
- Can be differentiated
- Can utilize GPUs for acceleration

Within FAIR, PyTorch3D has been used to power research projects such as [Mesh R-CNN](https://arxiv.org/abs/1906.02739).

## Installation

For detailed instructions refer to [INSTALL.md](INSTALL.md).

## License

PyTorch3D is released under the [BSD-3-Clause License](LICENSE).

## Tutorials

Get started with PyTorch3D by trying one of the tutorial notebooks.

|<img src="https://raw.githubusercontent.com/facebookresearch/pytorch3d/master/.github/dolphin_deform.gif" width="310"/>|<img src="https://raw.githubusercontent.com/facebookresearch/pytorch3d/master/.github/bundle_adjust.gif" width="310"/>|
|:-----------------------------------------------------------------------------------------------------------:|:--------------------------------------------------:|
| [Deform a sphere mesh to dolphin](https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/deform_source_mesh_to_target_mesh.ipynb)| [Bundle adjustment](https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/bundle_adjustment.ipynb) |

| <img src="https://raw.githubusercontent.com/facebookresearch/pytorch3d/master/.github/render_textured_mesh.gif" width="310"/> | <img src="https://raw.githubusercontent.com/facebookresearch/pytorch3d/master/.github/camera_position_teapot.gif" width="310" height="310"/>
|:------------------------------------------------------------:|:--------------------------------------------------:|
| [Render textured meshes](https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/render_textured_meshes.ipynb)| [Camera position optimization](https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/camera_position_optimization_with_differentiable_rendering.ipynb)|

| <img src="https://raw.githubusercontent.com/facebookresearch/pytorch3d/master/.github/pointcloud_render.png" width="310"/> | <img src="https://raw.githubusercontent.com/facebookresearch/pytorch3d/master/.github/cow_deform.gif" width="310" height="310"/>
|:------------------------------------------------------------:|:--------------------------------------------------:|
| [Render textured pointclouds](https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/render_colored_points.ipynb)| [Fit a mesh with texture](https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/fit_textured_mesh.ipynb)|

| <img src="https://raw.githubusercontent.com/facebookresearch/pytorch3d/master/.github/densepose_render.png" width="310"/> | <img src="https://raw.githubusercontent.com/facebookresearch/pytorch3d/master/.github/shapenet_render.png" width="310" height="310"/>
|:------------------------------------------------------------:|:--------------------------------------------------:|
| [Render DensePose data](https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/render_densepose.ipynb)| [Load & Render ShapeNet data](https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/dataloaders_ShapeNetCore_R2N2.ipynb)|

## Documentation

Learn more about the API by reading the PyTorch3D [documentation](https://pytorch3d.readthedocs.org/).

We also have deep dive notes on several API components:

- [Heterogeneous Batching](https://github.com/facebookresearch/pytorch3d/tree/master/docs/notes/batching.md)
- [Mesh IO](https://github.com/facebookresearch/pytorch3d/tree/master/docs/notes/meshes_io.md)
- [Differentiable Rendering](https://github.com/facebookresearch/pytorch3d/tree/master/docs/notes/renderer_getting_started.md)

### Overview Video

We have created a short (~14 min) video tutorial providing an overview of the PyTorch3D codebase including several code examples. Click on the image below to watch the video on YouTube:

<a href="http://www.youtube.com/watch?v=Pph1r-x9nyY"><img src="http://img.youtube.com/vi/Pph1r-x9nyY/0.jpg" height="225" ></a>

## Development

We welcome new contributions to PyTorch3D and we will be actively maintaining this library! Please refer to [CONTRIBUTING.md](./.github/CONTRIBUTING.md) for full instructions on how to run the code, tests and linter, and submit your pull requests.

## Contributors

PyTorch3D is written and maintained by the Facebook AI Research Computer Vision Team.

In alphabetical order:

* Amitav Baruah
* Steve Branson
* Luya Gao
* Georgia Gkioxari
* Taylor Gordon
* Justin Johnson
* Patrick Labtut
* Christoph Lassner
* Wan-Yen Lo
* David Novotny
* Nikhila Ravi
* Jeremy Reizenstein
* Dave Schnizlein
* Roman Shapovalov
* Olivia Wiles

## Citation

If you find PyTorch3D useful in your research, please cite our tech report:

```bibtex
@article{ravi2020pytorch3d,
    author = {Nikhila Ravi and Jeremy Reizenstein and David Novotny and Taylor Gordon
                  and Wan-Yen Lo and Justin Johnson and Georgia Gkioxari},
    title = {Accelerating 3D Deep Learning with PyTorch3D},
    journal = {arXiv:2007.08501},
    year = {2020},
}
```

If you are using the pulsar backend for sphere-rendering (the `PulsarPointRenderer` or `pytorch3d.renderer.points.pulsar.Renderer`), please cite the tech report:

```bibtex
@article{lassner2020pulsar,
    author = {Christoph Lassner},
    title = {Fast Differentiable Raycasting for Neural Rendering using Sphere-based Representations},
    journal = {arXiv:2004.07484},
    year = {2020},
}
```

## News

Please see below for a timeline of the codebase updates in reverse chronological order. We are sharing updates on the releases as well as research projects which are built with PyTorch3D. The changelogs for the releases are available under [`Releases`](https://github.com/facebookresearch/pytorch3d/releases),  and the builds can be installed using `conda` as per the instructions in [INSTALL.md](INSTALL.md).

**[November 2nd 2020]:** PyTorch3D v0.3 released, integrating the pulsar backend.

**[Aug 28th 2020]:**   PyTorch3D v0.2.5 released

**[July 17th 2020]:**   PyTorch3D tech report published on ArXiv: https://arxiv.org/abs/2007.08501

**[April 24th 2020]:**   PyTorch3D v0.2 released

**[March 25th 2020]:**   [SynSin](https://arxiv.org/abs/1912.08804) codebase released using PyTorch3D: https://github.com/facebookresearch/synsin

**[March 8th 2020]:**   PyTorch3D v0.1.1 bug fix release

**[Jan 23rd 2020]:**   PyTorch3D v0.1 released. [Mesh R-CNN](https://arxiv.org/abs/1906.02739) codebase released: https://github.com/facebookresearch/meshrcnn