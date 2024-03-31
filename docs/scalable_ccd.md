<center>
<h1>Time of Impact Dataset for Continuous Collision Detection and a Scalable Conservative Algorithm</h1>

<h3 style="margin-bottom:0;">
<a href="https://www.dbelgrod.com/">David&nbsp;Belgrod</a>,
<a href="https://cemse.kaust.edu.sa/people/person/bolun-wang">Bolun&nbsp;Wang</a>,
<a href="https://zferg.us">Zachary&nbsp;Ferguson</a>,
<a href="">Xin&nbsp;Zhao</a>,
<a href="https://publications.cnr.it/authors/marco.attene">Marco&nbsp;Attene</a>,
<a href="https://cims.nyu.edu/gcl/daniele.html">Daniele&nbsp;Panozzo</a>,
<a href="http://web.uvic.ca/~teseo/">Teseo&nbsp;Schneider</a>
</h3>

<center>*In submission*</center>
</center>


<figure>
    <img src="images/teaser.png">
    <figcaption style="margin:inherit 0; max-width:none; font-size:.8em; text-align: justify;">
        Approximate collision detection can lead to poor simulation results. We simulate this scene using Incremental Potential Contact [Li et al. 2020] which provides an intersection-free guarantee, but approximate collision detection (either broad- or narrow-phase) can break this guarantee. Here we see using an approximate broad-phase method (sweep and prune) results in missed collisions and intersections (see inset). In contrast, a conservative or exact method allows the ball to squeeze through the rollers and come out the bottom.
    </figcaption>
</figure>

---

## Paper

<b>
<!-- <a href="CCD-benchmark-paper.pdf">Paper (PDF)</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="CCD-benchmark-paper-350ppi.pdf">Low res (PDF)</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; -->
[arXiv](https://arxiv.org/abs/2112.06300)
</b>

## Abstract

We introduce a large-scale benchmark for broad- and narrow-phase continuous collision detection (CCD) over linearized trajectories with exact time of impacts and use it to evaluate the accuracy, correctness, and efficiency of 13 state-of-the-art CCD algorithms. Our analysis shows that several methods exhibit problems either in efficiency or accuracy.

To overcome these limitations, we introduce an algorithm for CCD designed to be scalable on modern parallel architectures and provably correct when implemented using floating point arithmetic. We integrate our algorithm within the Incremental Potential Contact solver [Li et al. 2020] and evaluate its impact on various simulation scenarios. Our approach includes a broad-phase CCD to quickly filter out primitives having disjoint bounding boxes and a narrow-phase CCD that establishes whether the remaining primitive pairs indeed collide. Our broad-phase algorithm is efficient and scalable thanks to the experimental observation that sweeping along a coordinate axis performs surprisingly well on modern parallel architectures. For narrow-phase CCD, we re-design the recently proposed interval-based algorithm of Wang et al. [Wang et al. 2021] to work on massively parallel hardware.

To foster the adoption and development of future linear CCD algorithms, and to evaluate their correctness, scalability, and overall performance, we release the dataset with analytic ground truth, the implementation of all the algorithms tested, and our testing framework.

## Video

<div class="video-wrapper">
<iframe class="youtube" src="https://www.youtube-nocookie.com/embed/ezuC9EisPII?si=_oZJwrSBQa5zV6WT" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

## Source Code and Data

[![Build](https://github.com/continuous-collision-detection/scalable-ccd/actions/workflows/continuous.yml/badge.svg)](https://github.com/continuous-collision-detection/scalable-ccd/actions/workflows/continuous.yml)
[![License](https://img.shields.io/github/license/continuous-collision-detection/scalable-ccd.svg?color=blue)](https://github.com/continuous-collision-detection/scalable-ccd/blob/main/LICENSE)

* [Our Scalable CCD](https://github.com/Continuous-Collision-Detection/Scalable-CCD)
* [Algorithms and Testing Framework]() (coming soon!)
* Data:
    * [Sample](https://github.com/Continuous-Collision-Detection/Sample-Scalable-CCD-Data)
    * [Full Dataset]() (coming soon!)

## BibTex

```bibtex
@misc{Belgrod:2023:Time,
    title        = {Time of Impact Dataset for Continuous Collision Detection and a Scalable Conservative Algorithm},
    author       = {David Belgrod and Bolun Wang and Zachary Ferguson and Xin Zhao and Marco Attene and Daniele Panozzo and Teseo Schneider},
    year         = 2023,
    eprint       = {2112.06300},
    archivePrefix= {arXiv},
    primaryClass = {cs.GR}
}
```

## Acknowledgments

We thank the NYU IT High Performance Computing for resources, services, and staff expertise. This work was funded by the NSF CAREER award under Grant No. 1652515, the NSF grants OAC-1835712, OIA-1937043, CHS-1908767, CHS-1901091, NSERC DGECR-2021-00461 and RGPIN 2021-03707, KAUST baseline funding (grant BAS/1/1679-01-01), by EU project DIGITbrain/ProMED (952071).