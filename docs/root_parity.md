<center>
<h1>Fast and Exact Root Parity for Continuous Collision Detection</h1>

<h3 style="margin-bottom:0;">
<a href="https://cemse.kaust.edu.sa/people/person/bolun-wang">Bolun Wang</a>,
<a href="https://zferg.us">Zachary Ferguson</a>,
<a href="">Xin Jiang</a>,
<a href="https://publications.cnr.it/authors/marco.attene">Marco Attene</a>,
<a href="https://cims.nyu.edu/gcl/daniele.html">Daniele Panozzo</a>,
<a href="http://web.uvic.ca/~teseo/">Teseo Schneider</a>
</h3>

<center>*Computer Graphics Forum (Eurographics), 2022*</center>
</center>


<figure>
    <img src="images/vf.png" width="45%" style="display:inline-block;margin-left:auto;margin-right:10px">
    <img src="images/ee.png" width="45%" style="display:inline-block;margin-left:10px;margin-right:auto">
    <figcaption style="margin:inherit 0; max-width:none; font-size:.9em; text-align: justify;">
        The parity of the roots between a moving triangle and a point (left) and between two moving edges (right), can be computed by counting the parity of the intersections of a ray (red) casted from the origin (red sphere) with the surface of a prism for the vertex-triangle case (left) or a cube for the edge-edge case (right).
    </figcaption>
</figure>

---

## Paper

<b>
<a href="root-parity-ccd-paper.pdf">Paper (PDF)</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="root-parity-ccd-paper-350ppi.pdf">Low res (PDF)</a>
</b>

## Abstract

We introduce the first **exact** root parity counter for continuous collision detection (CCD). That is, our algorithm computes the parity (even or odd) of the number of roots of the cubic polynomial arising from a CCD query. We note that the parity is unable to differentiate between zero (no collisions) and the rare case of two roots (collisions).

Our method does not have numerical parameters to tune, has a performance comparable to efficient approximate algorithms, and is exact. We test our approach on a large collection of synthetic tests and real simulations, and we demonstrate that it can be easily integrated into existing simulators.

## Fast Forward

<div class="video-wrapper">
<iframe class="youtube" src="https://www.youtube-nocookie.com/embed/3nXvf1nI23M?si=90pItnlHagyD2Qb7" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

## Presentation

* Watch our full Eurographics 2022 presentation on [Bilibili](https://www.bilibili.com/video/BV12U4y1U7nV/) (English)!

<div class="video-wrapper">
<iframe class="youtube" src="https://www.youtube-nocookie.com/embed/HoEbM0fN9Wk?si=Qf76VOh03dV-PkLj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

## Simulation Videos

<figure>
    <video width="100%" controls>
        <source src="videos/octocat-soup.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <figcaption style="margin:inherit 0; max-width:none; text-align: justify;">
        We drop three elastic Octocats into a bowl and use our CCD within a filtered line search to keep the meshes intersection-free (simulated using IPC [Li et al. 2020] with a timestep of 0.07s).
    </figcaption>
    <video width="100%" controls>
        <source src="videos/mat-twist.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <figcaption style="margin:inherit 0; max-width:none; text-align: justify;">
        We run the mat-twist experiment from [Li et al. 2020] using our CCD method in the filtered line-search and timestep of 0.04 s. The mat is 1m × 1m × 8mm and our algorithm conservatively shifts the world by [11.75, 11.75, 12.24] which results in a rounding error of 2.66e-15.
    </figcaption>
</figure>

## Source Code and Data

<a href="https://github.com/Continuous-Collision-Detection/ExactRootParityCCD/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/Continuous-Collision-Detection/ExactRootParityCCD.svg?color=blue"></img>
</a>

* [Code](https://github.com/Continuous-Collision-Detection/ExactRootParityCCD)
* [Dataset of Rounded CCD Queries](https://archive.nyu.edu/handle/2451/63808)

## BibTex

```bibtex
@article{Wang:2022:FastRootParity,
	title        = {Fast and Exact Root Parity for Continuous Collision Detection},
	author       = {Bolun Wang and Zachary Ferguson and Xin Jiang and Marco Attene and Daniele Panozzo and Teseo Schneider},
	year         = 2022,
	journal      = {Computer Graphics Forum (Proceedings of Eurographics)},
	volume       = 41,
	number       = 2,
	numpages     = 9
}
```

## Acknowledgments

We thank the NYU IT High Performance Computing for resources, services, and staff expertise.
This work was partially supported by the NSF CAREER award under Grant No. 1652515, the NSF grants OAC-1835712, OIA-1937043, CHS-1908767, CHS-1901091, National Key Research & Development Program of China Grant No. 2020YFA0713701, Natural Science Foundation of China Grants No.~12171023 & No. 12001028, NSERC DGECR-2021-00461 and RGPIN-2021-03707, EU ERC Advanced Grant CHANGE No. 694515, a Sloan Fellowship, a gift from Adobe Research, a gift from nTopology, and a gift from Advanced Micro Devices, Inc.
