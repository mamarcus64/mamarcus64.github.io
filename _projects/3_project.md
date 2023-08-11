---
layout: page
title: Amazon
description: Software development intern.<br>May 2022 - Aug 2022. Boston, MA.
img: assets/img/7.jpg
importance: 3
category: 2022
learn_more: A summer of firsts for me - first time working at an established tech company, first time living by myself, and first time in the beautiful city of Boston. I'm just lucky I wasn't there for the winter; I don't think my weak California pysche could take anything that cold. At AWS, I was working with the RDS PostgreSQL Team, which to my chagrin, did not mean writing SQL commands for twelve weeks. Turns out, we were working ON Postgres, which means diving deep into a labyrinth of C code that was mostly written before I was even born. (Seriously, I found several comments that were timestamped from 1989). My project was focused on speeding up the SQL JOIN function by implementing semi-join hashing with <a href="https://web.stanford.edu/~balaji/papers/bloom.pdf"> Bloom filters </a> during a Merge Join to eliminate unnecessary table rows early on in the execution tree. Essentially, Merge Join is a join strategy that is very similar to Mergesort, which is great because it runs in O(n log n) time. However, it turns out that even this operation can be made more efficient - by scanning one side of the join and mapping it into a Bloom filter, which is essentially a low-storage probabilistic hash map, large swathes of the other join table can be removed if their distributions do not overlap much. I implemented this optimization into AWS' Postgres as well as a decision planner (based on a heuristic of the aforementioned distribution overlap) to decide when to actually execute it. Overall, this implementation was a success, increasing query speeds by up to 36% on ideal queries and improved our performance on the <a href="https://www.tpc.org/tpch/"> standard database benchmark TPC-H </a> by about 5%.
proj_id: aws_2
# last_loaded: true
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
