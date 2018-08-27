# TerraVoxel ->  more voxel more Adidas

Goal: Reach 1 Terravoxel at interactive speeds with current midrange hw.

Current State:
[67 Milion voxels Online Demo](https://terravoxel.appspot.com)
Viewable around 10M on mine crappy old notebook Intel Hd 3000 embeded GPU in (i5 cpu from 2011)

Bugs:

Depending on camera angle depth sorting breaks
Frustrum culling not working efficiently. When near surface still milions faces are being rendered.

To Do:

add loading of image tiles like google maps and move slow one 7mb image loading away as soon as possible.
Or github guys will killme ;(

Add more vogels to currently empty faces via parallax mapping thus reaching 1 Teraa voxel?.


The aim of this project is to squeeze maximum number of cubes/voxels from HW.
Currently it uses  one voxel per triangle transparency trick that come to my mind a day ago and hw instancing.

Ie in the middle of every triangle is essentially quad with tris on sides by making tris transparent only quad part remains visible.
Advantage is that we can push twice as much faces as oposed to classic 2 triangle per quad on any hw.
The price we pay for this are depth sorting  zorder issues associated with transparency.

Since sorting milions of tris on cpu is not feasible one sollution is flipping meshes and its uv coordinates (TODO:)
every 180 camera angle thus preserving back to front rendering order (classic painters algo)

Future:

I plan to collect further benchmarks on a lot of interesting mobile gpu.
I will be able to do this all for free on many expensive devices. How?

All thx to fantastic support of Open Source projects form wonderfull people at http://www.BrowserStack.com. 
