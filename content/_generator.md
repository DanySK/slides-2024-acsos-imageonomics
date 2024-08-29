
+++

title = "Decentralized Multi-Drone Coordination for Wildlife Video Acquisition"
description = "ACSOS 2024 main-track paper presentation"
outputs = ["Reveal"]

+++

{{< slide background-image="zebras.jpg" >}}

<div
style="
position: fixed;
/* bottom: 0;
right: 0; */
font-size: .3em;
top: 800px;
left: 50%;
transform: translate(-50%, -50%);
"
>background image adapted from: Diego Delso, delso.photo, License CC BY-SA</div>

# Decentralized Multi-Drone Coordination for Wildlife Video Acquisition

[Denys Grushchak](denys.grushchak@studio.unibo.it) <i class="fa-solid fa-computer"></i>,
[Jenna Kline](kline.377@osu.edu) <i class="fa-solid fa-horse"></i>,
[Danilo Pianini](danilo.pianini@unibo.it) <i class="fa-solid fa-computer"></i>, <br>
[Nicolas Farabegoli](nicolas.farabegoli@unibo.it) <i class="fa-solid fa-computer"></i>,
[Gianluca Aguzzi](gianluca.aguzzi@unibo.it) <i class="fa-solid fa-computer"></i>,
[Martina Baiardi](m.baiardi@unibo.it) <i class="fa-solid fa-computer"></i>,
and
[Christopher Stewart](cstewart@cse.ohio-state.edu) <i class="fa-solid fa-horse"></i>

{{% multicol %}}
{{% col %}}
<div style="text-align: center; width: 100%;">
<img src="example-background.svg" style="width: 50%" />
</div>

<i class="fa-solid fa-computer"></i> Department of Computer Science and Engineering, University of Bologna, Cesena (FC), Italy
{{% /col %}}
{{% col %}}
<div style="text-align: center; width: 100%;">
<img src="osu.svg" style="width: 50%" />
</div>

<i class="fa-solid fa-horse"></i> Computer Science and Engineering Department, The Ohio State University, Columbus (OH), USA
{{% /col %}}
{{% /multicol %}}

---

{{< slide background-image="zebras.jpg" >}}

# Wildlife behavior acquisition

A paramount tool for *ethologists* and *biologists* to gather insights into the nature and inform
**conservation** efforts for **endangered species**.

* {{% fragment %}} Animal *health* monitoring {{% /fragment %}}
* {{% fragment %}} *Behavioral changes* induced by *climate change* or *human activity*{{% /fragment %}}
* {{% fragment %}} Current *population level*{{% /fragment %}}
* {{% fragment %}} Insights into *future population levels*{{% /fragment %}}

---

{{< slide background-image="collar.jpg" >}}

<div
style="
position: fixed;
/* bottom: 0;
right: 0; */
font-size: .3em;
top: -500px;
left: 50%;
transform: translate(-50%, -50%);
"
>background image: Abujoy, License CC BY-SA</div>

---

{{< slide background-image="collarblur.jpg" >}}

<div
style="
position: fixed;
/* bottom: 0;
right: 0; */
font-size: .3em;
top: -500px;
left: 50%;
transform: translate(-50%, -50%);
"
>background image derived from: Abujoy, License CC BY-SA</div>

---

{{< slide background-image="collarblur2.jpg" >}}

# GPS collars

* {{% tick %}} Great position tracking
* {{% tick %}} Possibly equipped with further sensors (temperature, accelerometer...)
* {{% tick %}} Long battery life
* {{% cross %}} No video
* {{% cross %}} Invasive (requires capture and release) $\Rightarrow$ Limited sample size

---

{{< slide background-image="trap.jpg" >}}

<div
style="
position: fixed;
/* bottom: 0;
right: 0; */
font-size: .3em;
top: -500px;
left: 0%;
transform: translate(-50%, -50%);
color: white;
"
>author: Arddu, License CC Attribution 2.0 Generic</div>

---

{{< slide background-image="trap2.jpg" >}}

<div
style="
position: fixed;
/* bottom: 0;
right: 0; */
font-size: .3em;
top: -500px;
left: 0%;
transform: translate(-50%, -50%);
color: white;
"
>author: Winterline, License CC Attribution-Share Alike 3.0 Unported</div>

---

{{< slide background-image="trap3.jpg" >}}

<div
style="
position: fixed;
/* bottom: 0;
right: 0; */
font-size: .3em;
top: -500px;
left: 0%;
transform: translate(-50%, -50%);
color: white;
"
>author: Kalyan Varma, License CC BY-SA</div>

---

{{< slide background-image="trap3-blur.jpg" >}}

---

{{< slide background-image="trap-setup.jpg" >}}

<div
style="
position: fixed;
/* bottom: 0;
right: 0; */
font-size: .3em;
top: -500px;
left: 0%;
transform: translate(-50%, -50%);
color: blue;
"
>author: Prashanthns, License CC BY-SA</div>

---

{{< slide background-image="trap-setup-blur.jpg" >}}

# Camera traps

* {{% tick %}} Photos and potentially videos
* {{% tick %}} Non-invasive
* {{% tick %}} Multiple species
* {{% cross %}} Static and with limited range
* {{% cross %}} False triggers
* {{% cross %}} Subject to vandalism and theft
* {{% cross %}} Generally fragile (the tiger in the first picture destroyed the camera)

---

{{< slide background-video="nadir.mkv" background-video-loop="true" background-video-muted="true" >}}

---

{{< slide background-video="nadir.mkv" background-video-loop="true" background-video-muted="true" background-opacity="0.2" >}}

# Fixed-wing drone aerial views


* {{% tick %}} *Very large area* coverage
* {{% tick %}} *Long flights*
* {{% cross %}} **Nadir** imagery: good for mapping, bad for *individual behavior*
* {{% cross %}} Requires *specialized training*
* {{% cross %}} *Predefined* flight paths

---

{{< slide background-video="nonnadir.mkv" background-video-loop="true" background-video-muted="true" >}}

---

{{< slide background-video="nonnadir.mkv" background-video-loop="true" background-video-muted="true" background-opacity="0.5" >}}

## Non-nadir perspective

![](non-nadir-fov.svg)

---

{{< slide background-video="nonnadir.mkv" background-video-loop="true" background-video-muted="true" background-opacity="0.2" >}}

# Quadcopters and similar drones

{{% multicol %}}
{{% col %}}
* {{% tick %}} *Large area* coverage
    * Although much *smaller than fixed-wing* drones
* {{% tick %}} **Non-Nadir** view is great for *individual behavior*
* {{% tick %}} **Multiple** drones can get *different perspectives*
* {{% tick %}} **Dynamic trajectories**
* {{% cross %}} *Noise* may disturb wildlife
* {{% cross %}} *Skilled pilots* required
    * {{% cross %}} **Practically impossible** to coordinate multiple drones effectively by hand
* {{% cross %}} Relatively *short battery life*
{{% /col %}}
{{% col %}}
{{% fragment %}}
### $\Rightarrow$ **Multi-Drone Coordination**
* *No* need for *human pilots*
* Similar to *well-known problems in the literature*!
{{% /fragment %}}
{{% /col %}}
{{% /multicol %}}

---

{{< slide background-image="zebras.jpg" >}}

# A special OMOkC

In the *Online Multi-Object k-Coverage* (**OMOkC**) problem,
dones coordinate to cover each *interesting* target with at least $k$ points of view.

<iframe width="888" height="500" src="https://www.youtube.com/embed/yuaY_8Vr3oc?si=2iViF8GqIg8z8NCF&amp;start=5&amp;autoplay=1&amp;loop=1&amp;playlist=yuaY_8Vr3oc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share; loop" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Our problem is a variant of , in which:

1. {{% fragment %}}The focus is on animal *groups* rather than single animals $\Rightarrow$ **Herd tracking**{{% /fragment %}}
2. {{% fragment %}}Drones have a *blind zone* due to their non-nadir point of view $\Rightarrow$ **Blind zone**{{% /fragment %}}
3. {{% fragment %}}The *position* of animals within the Field-of-View dramatically changes the quality of the result $\Rightarrow$ **FoV centrality**{{% /fragment %}}
4. {{% fragment %}}The *angle* at which a subject is being observed matters, lateral views are more informative than frontal ones $\Rightarrow$ **Observation angle**{{% /fragment %}}
5. {{% fragment %}}Observers emit *noise* that may alter the behavior of the observed animals $\Rightarrow$ **Noise pollution**{{% /fragment %}}
6. {{% fragment %}}Observation is performed in contexts with *limited infrastructure* $\Rightarrow$ **Decentralized coordination**{{% /fragment %}}

---

{{< slide background-image="zebras.jpg" >}}

# Contribution

## A methodology to evaluate the performance in wildlife video acquisition

We define **metrics** for:
1. The *centrality* in the Field-of-View of each camera
2. The overall *angles* of observation of each animal
3. The *noise* pollution generated by the drones

We build simulations based on a novel *herd simulation* algorithm based on the [KABR dataset](https://doi.ieeecomputersociety.org/10.1109/WACVW60836.2024.00011)<br>
(Jenna presented the algorithm at SISSY on Monday)

{{% fragment %}}

$\Rightarrow$ We observe that *pre-existing OMOkC algorithms do not perform as well as expected in our context*,
and thus we propose to extend the current SOTA with:

## An herd-aware decentralized multi-drone coordination algorithm

{{% /fragment %}}

---

{{< slide background-image="zebras.jpg" >}}

# FoV Centrality

* Let $P_c$ be the center of the FoV $\mathcal{V}$ of camera $c$.
* Let $F(c)$ be the maximum distance from the center of the FoV

then

$F(c) = \max \left\| P - P_c \right\| ~ \forall P \in \mathcal{V}$.

* For any camera $c$, *$F(c)$* represents the *worst possible position* in its FoV.
* For an animal $z$ located in $P_z$, a normalized estimate of *how poorly* it is positioned in the FoV of $c$ is:
the ratio between its distance to the center and $F(c)$:
$\frac{\left\| P_z - P_c \right\|}{F(c)}$
* The *normalized FoV centrality* for a target animal $z$ and a drone $c$ is then: $Q(z, c) = 1 - \frac{\left\| P_z - P_c \right\|}{F(c)}$
* Generalized for a set of cameras $C$ observing a target $z$: $\Gamma(z) = \max_{c \in C} Q(z, c)$

{{% fragment %}}
{{% multicol %}}{{% col %}}
### TL;DR: the closer to the center, the better
* find the *worst possible position* to be used as *bound*
* use that to estimante *how good is the **animal** position for **each camera***
* *for **each animal***, *consider only the **best camera***
{{% /col %}}{{% col %}}
![fov-centrality](fov-centrality.svg)
{{% /col %}}{{% /multicol %}}
{{% /fragment %}}

---

{{< slide background-image="zebras.jpg" >}}

# Observation angle: body coverage

**Ideas**
1. the best observation comes from a perfectly *perpendicular angle*
2. the "*longer*" *the side* of the animal that is being observed, the better the observation
    * that's why observations from the side are more valuable than frontal or back ones
3. *small deviations* from perpendicularity are not that bad

![](body-coverage-metric.svg)

1. *approximate* the animal's body with a polygon
2. for each segment $s$ find the camera $c$ observing the segment midpoint from the smallest angle $\alpha_s$: $c$ has the best available view for $s$
3. normalize $\alpha_s$ in $[0, 1]$ with $\Phi: [-\frac{\pi}{2}, \frac{\pi}{2}]\rightarrow{}[0, 1]$.
4. use a logistic function to penalize more the *extreme* angles: $\Phi(x;\mu,\nu)=\left[1+\left(\frac{x(1-\mu)}{\mu(1-x)}\right)^{-\nu}\right]^{-1}, \mu=\frac{1}{2}, \nu=5$
5. get the *observation quality* for $s$: $\xi(s) = \Phi\left(\frac{|\alpha_s|}{\frac{\pi}{2}}; \frac{1}{2}, 5\right)$.
6. *repeat for every "side"* of the animal in $S_z$ to get the **body coverage** $\Diamond(z) = \frac{\sum_{s \in{} S_z} \|s\| \cdot \xi(s)}{\|S_z\|}$


---

{{< slide background-image="zebras.jpg" >}}

# Noise pollution

We need the *Sound Pressure Level* $L_P$ at the position of the animal.

Of course, manufacturers only provide the *Sound Power Level* $L_W$, a measure of the sound energy emitted by the drone.

To convert into the SPL at distance $r$ from the drone, we need a *directivity factor $Q$*:
$L_P = L_W - \left| 10 \log_{10} \left(\frac{Q}{4 \pi r^{2}}\right) \right| $

We assume $Q=1$ (*spherical propagation*), and $r=1m$ (a *typical distance* at which manifacturer measure the Sound Power Level).

The $L_P$ perceived by an animal $z$ at distance $d$ from the drone
with air attenuation is:
$ L_{P_d}(z) = L_{P}(z) + 20 \log_{10} \left(\frac{r}{d}\right)$

For multiple drones $C$, their contributions sum:
$L_{P_T}(z) = 10 \log_{10} \left(\sum_{c \in{C}} 10^{\frac{L_{P_c}(z)}{10}} \right)$

To *normalize* in $[0, 1]$, we assume that *a noise below $20dB$* (~ a ticking watch) can't be distinguished from the background,
and *a noise above $80dB$* (~ police car siren) will *always* disturb the animal.

Since noise is perceived non-linearly, we use a sigmoid with
$\mu=40dB$ (~ *refrigerator hum*, our proxy for the *background noise*).

The final *normalized noise metric* is thus $\rho(z) = \Phi\left(h(L_{P_T}(z)); h(\mu), 4\right)$

{{% fragment %}}
### TL;DR
* we assume noise **propagates in air** without major obstacles or reflections
* we set **silence** at the sound of a ticking watch, and **maximum noise** at the level of a police siren
* we sum the contribution of **every drone** and consider **non-linear perception**
{{% /fragment %}}

---

{{< slide background-image="zebras.jpg" >}}

# Herd-sensitive tracking

Running state-of-the-art OMOkC algorithms¹ on our setup highlighted some issues:
* OMOkC algorithms are designed to cover *individual* targets, not *groups*
* Current SOTA algorithms are meant to quickly react to *changes in interestingness*, but all animals are equally interesting
* Usual setups have enough drones to provide $k$ views for each target, but with herds *targets largely outnumber* drones

### $\Rightarrow$ We alter the general structure of OMOkC algorithms to track herd centroids instead of individual targets.

1. **Identification and localization**: each drone identifies and localizes the animals in its FoV as best as it can
    * we accept localization and identification errors
2. **Information exchange and consensus**: local information is exchanged among drones to reach consensus on the herd composition,
then each drone, locally, performs a *recursive hierarchical agglomerative clustering*² to find the *herd centroid*
    * we accept limited communication ranges and network segmentation
    * we accept that different drones may have different information and compute different centroids
3. **Prioritization**: we feed the locally-computed herd centroids to the original OMOkC algorithms

<span style="text-align: left; font-size: 0.5em; position: absolute; left: 0em; bottom: -10em">

1. [D. Pianini, F. Pettinari, R. Casadei, and L. Esterle, “A collective adaptive approach to decentralised k-coverage in multi-robot systems,” ACM Trans. Auton. Adapt. Syst., vol 17, pp. 4:1–4:39, 2022.](https://doi.org/10.1145/3547145)
2. [A. Lukasová, “Hierarchical agglomerative clustering procedure,” Pattern Recognit. 11(5-6): 365-381, 1979](https://doi.org/10.1016/0031-3203(79)90049-9)

</span>

---

# Evaluation

* Simulation of a 2x2km arena realized in Alchemist¹, algorithms written in Protelis²
    * aggregate computing³ worked quite well for the decentralized coordination
* video capture session of 30 minutes (to avoid concerns related to battery life)
* 140 grazing zebras, moving at a maximum speed of $2\frac{m}{s}$ split in 2, 4, or 8 separate herds
* *drone-to-herd ratio* of 1:1, 2:1, and 3:1.
* drones can move at $10\frac{m}{s}$ and have a line-of-sight communication range of $1km$.

<span style="text-align: left; font-size: 0.5em; position: absolute; left: 0em; bottom: -15em">

1. <img src="https://alchemistsimulator.github.io/images/logo.svg" style="width: 2em; margin-top: 0px; margin-bottom: 0px" /> https://alchemistsimulator.github.io/
2. <img src="https://github.com/Protelis/Protelis.github.io/raw/da40bb7c50d49683ce8ea9d32aab71cf225bd23d/images/2018-03-16-protelis-icon.svg" style="width: 2em; margin-top: 0px; margin-bottom: 0px" /> https://protelis.github.io/
3. [Aggregate Programming for the Internet of Things. Computer 48(9): 22-30 (2015)](https://doi.org/10.1109/MC.2015.261)

</span>

---

# Future work

* Robustness analysis
* Noise-sensitive herds
* Energy model and management

# Headers

# H1
## H2
### H3
#### H4

---

# Text

normal text

`inline code`

*italic*

**bold**

**_emphasized_**

*__emphasized alternative__*

~~strikethrough~~

[link](http://www.google.com)

---

# Lists and enums

1. First ordered list item
1. Another item
    * Unordered sub-list.
    * with two items
        * another sublist
            1. With a sub-enum
            1. yay!
1. Actual numbers don't matter, just that it's a number
  1. Ordered sub-list
1. And another item.

---

# Inline images

![Alternative text](https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg)

---

## Fallback to shortcodes for resizing

Autoresize specifying

* `max-w` (percent of parent element width) and/or `max-h` (percent of viewport height) as max sizes , and
* `width` and/or `height` as *exact* sizes (as percent of viewport size)

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" height="20">}}

---

## Multi-column slide

{{% multicol %}}{{% col %}}
Column 1
{{% /col %}}{{% col %}}
Column 2
{{% /col %}}{{% /multicol %}}

---

## Tick and Cross

{{% tick %}} This is something good
{{% cross %}} This is something good

---

## Chart.js

{{< chart >}}
{
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: 'Bar Chart',
            data: [12, 19, 18, 16, 13, 14],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        maintainAspectRatio: false,
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
}
{{< /chart >}}

---

## FontAwesome

<i class="fa-solid fa-mug-hot"></i>
<i class="fa-solid fa-lemon"></i>
<i class="fa-solid fa-flask"></i>
<i class="fa-solid fa-apple-whole"></i>
<i class="fa-solid fa-bacon"></i>
<i class="fa-solid fa-beer-mug-empty"></i>
<i class="fa-solid fa-pepper-hot"></i>

---

## Bootstrap 1

<div class="card w-100" >
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e9/View_of_Cesena_from_the_Abbey.jpg/1920px-View_of_Cesena_from_the_Abbey.jpg" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>

---

## Bootstrap 2

<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>

<button type="button" class="btn btn-link">Link</button>

---

## Low res, plain markdown

![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Scavolino_innevata.jpg/260px-Scavolino_innevata.jpg)

---

## Hi res, plain markdown

![](https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg)

---

## Low res, default

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Scavolino_innevata.jpg/260px-Scavolino_innevata.jpg" >}}

---

## Hi res, default

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" >}}

---

## Low res, enlarged horizontally

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Scavolino_innevata.jpg/260px-Scavolino_innevata.jpg" width="100">}}

---

## Low res, enlarged vertically

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Scavolino_innevata.jpg/260px-Scavolino_innevata.jpg" height="100">}}

---

## Hi res, reduced horizontally

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" width="50">}}

---

## Hi res, reduced vertically

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" height="50">}}

---

## Hi res, reducing maximum expansion horizontally

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" width="50">}}

---

## Hi res, reducing maximum expansion vertically

{{< figure src="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" height="50">}}

---

{{< slide background-image="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" >}}

# Large images as background
## (May affect printing)

---

{{< slide background-image="https://upload.wikimedia.org/wikipedia/commons/6/6c/Scavolino_innevata.jpg" state="blur-animation-light"  transition="fade-in fade-out" >}}

# Also available with blur and custom transitions
## (May affect printing)

---

# $$\LaTeX{}$$


Inline equations like $E=mc^2$

$$\frac{n!}{k!(n-k)!} = \binom{n}{k}$$

---

# Code snippets


```kotlin
val x = pippo
```

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello world!")
}
```

---

# Tables

Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the
raw Markdown line up prettily. You can also use inline Markdown.

---

# Quotes

> Multiple
> lines
> of
> a
> single
> quote
> get
> joined

> Very long one liners of Markdown text automatically get broken into a multiline quotation, which is then rendered in the slides.

---

# Fragments

* {{< frag c="pluto" >}}
* {{< frag c="pluto" >}}
* {{< frag c="pluto" >}}

---

# Graphs via Gravizo

{{< gravizo "Example Gravizo graph" >}}
  digraph G {
    aize ="4,4";
    main [shape=box];
    main -> parse [weight=8];
    parse -> execute;
    main -> init [style=dotted];
    main -> cleanup;
    execute -> { make_string; printf}
    init -> make_string;
    edge [color=red];
    main -> printf [style=bold,label="100 times"];
    make_string [label="make a string"];
    node [shape=box,style=filled,color=".7 .3 1.0"];
    execute -> compare;
  }
{{< /gravizo >}}

---

# Graphs via mermaid.js

```mermaid
classDiagram
  Class01 <|-- AveryLongClass : Coosssl
  Class03 *-- Class04
  Class05 o-- Class06
  Class07 .. Class08
  Class09 --> C2 : Where am i?
  Class09 --* C3
  Class09 --|> Class07
  Class07 : equals()
  Class07 : Object[] elementData
  Class01 : size()
  Class01 : int chimp
  Class01 : int gorillasaaaaaaaaaaaaaaaaaaaaaa
  Class08 <--> C2: Cool label
```

---


# Graphs via mermaid.js with options

```mermaid
%%{init: {'theme':'default', 'themeVariables': { 'fontSize': '.34em', 'fontFamily': 'verdana' }}}%%
classDiagram
  Class01 <|-- AveryLongClass : Coosssl
  Class03 *-- Class04
  Class05 o-- Class06
  Class07 .. Class08
  Class09 --> C2 : Where am i?
  Class09 --* C3
  Class09 --|> Class07
  Class07 : equals()
  Class07 : Object[] elementData
  Class01 : size()
  Class01 : int chimp
  Class01 : int gorillasaaaaaaaaaaaaaaaaaaaaaa
  Class08 <--> C2: Cool label
```


---
# Graphs via mermaid.js 2

```mermaid
graph TD
  SL([fa:fa-user second level]) --> L[solution]
  L -- solution email --> db[(mysql)]
  db --> X[automatic]
  X --> CM([fa:fa-users first level])
  db -- Email --> c([customer support]);
```

---

# Graphs via mermaid.js 3

```mermaid
gitGraph
  commit id: "Initialize project"
  commit id: "Make some changes"
  branch develop
  checkout develop
  commit
  commit
  checkout main
  merge develop
  commit
  commit
```

---

# Keystrokes

<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Del</kbd>

---

# Import shared slides

<!-- write-here "shared-slides/devops/devops-intro.md" -->
<!-- end-write -->
