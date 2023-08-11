---
layout: page
title: Forschungszentrum Jülich
description: DAAD scholar research intern. <br> Aug 2022 - Oct 2022. Jülich, Germany.
img: assets/img/3.jpg
importance: 2
category: 2022
proj_id: julich
learn_more: Say what you will about the Germans, but they love their hard work and their long words. When I first arrived at the IEK-10 Lab at Forschungszentrum Jülich they immediately had me sign my Arbeiterunfallverischerungsgesetz paperwork and before I could even take a sip of my Mineralwasser (lemon-flavored!), gave me a two-hour lecture on how their lab applied novel artificial intelligence and traditional linear programming towards solving energy-grid problems in the nearby region. Luckily for me, it was in English. Needless to say, my foray into Europe was a continuous stream of new and interesting experiences and my research project there was just as captivating. I was studying different methods for verifiable robustness for neural networks, which refers to the concept of maintaining classification accuracy within a region of input perturbations. To clarify, a classic example of a non-robust network is the image classifier that can recognize an image of a stop sign, but classifies it as a cat if you change the RGB value of just a few pixels. Typically, the standard method of creating robust models, <a href="https://arxiv.org/abs/1810.12715">Interval Bound Propogation (IBP)</a>, is to replace an input datum with a fixed-size orthongonal bounding box, which represents the epsilon of error to account for, and to propogate this box over each layer and to relax this constraint into another bounding box to make the problem tractable. I was tasked with investigating <a href="https://psor.uconn.edu/wp-content/uploads/sites/1972/2016/10/Generalized-McCormick-relaxations-Scott-et-al-2011.pdf">McCormick relaxations </a> as a layer propogation technique, where each layer's bounding box would be defined by the convex and concave relaxations of the associated layer function. This has the benefit of still being tractable, as these functions are continuous and monotonic, but these relaxations are in theory much tighter than the orthogonal boxes of IBP. Overall, like many academic projects, my investigation was a half-success. While my results did find that McCormick relaxations are about 40% tigher than IBP, calculating them took significantly longer (this is because McCormick relaxation calulations grow quadratically with dimension size, while two points will always define an orthongonal box). So for now, IBP remains on the throne, but maybe we'll see a McCormick comeback if processing power ever catches up!
---

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
