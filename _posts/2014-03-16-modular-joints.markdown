---
layout: post
title: "Modular Joints"
date: 2014-03-16
---

Here's a fun, Project Euler-esque brain exercise:<br>
You're given bars of 28" X 1" X 1" square iron.
Each bar has on one end, a 1/4" bracket at the first quarter inch, and at the other end, a 1/4" bracket at the third quarter inch. Let's call these the 1 and 3 ends, respectively. The bars can be flipped over, creating ends 2 and 4.
<br>
By flipping and rotating these bars, build a 4X4 modular grid where each bracket is adjacent to another bracket. For example, a 2 can be connected to a 1 or 3. But 3 must be present before it can connect to a 4. A 4 can only connect to a 3.
</div><div class="container">
<img src="{{ site.baseurl }}media/grid.jpg" width="300" height="400">
</div>
<br>
This came about from my architecture project. Without going into too much detail (my team is in a contest), the professor has challenged us to make a design that's as modular as possible. Right now we have 3 pieces to our design: skeleton, joints, and surface panels. The object of this problem is to integrate the joints into the skeleton, leaving us with just two pieces. If this can work out, it would be visually boring yet elegant and esoterically beautiful.
