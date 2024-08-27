
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


* {{% tick %}} *Large area* coverage
* {{% tick %}} *Long flights*
* {{% cross %}} **Nadir** imagery: good for mapping, bad for *individual behavior*
* {{% cross %}} Requires *specialized training*
* {{% cross %}} *Predefined* flight paths

---

{{< slide background-video="nonnadir.mkv" background-video-loop="true" background-video-muted="true" >}}

---

{{< slide background-video="nonnadir.mkv" background-video-loop="true" background-video-muted="true" background-opacity="0.2" >}}

# Quadcopters and similar drones

* {{% tick %}} *Large area* coverage
* {{% tick %}} **non-Nadir** great for *individual behavior*
* {{% tick %}} **Multiple** drones can get *different perspectives*
    * {{% cross %}} **Practically impossible** to coordinate by hand
* {{% cross %}} *Noise* may disturb wildlife
* {{% cross %}} *Skilled pilots* required
* {{% cross %}} Relatively *short battery life*

![](non-nadir-fov.svg)

---

{{< slide background-iframe="https://www.youtube.com/embed/c0FtiZUO9Kg?si=hKEZcilEFRt_xx1c&autoplay=1&controls=0&showinfo=0&autohide=1" background-interactive="true" >}}

---


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
