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

It can be interesting to optimize for / collect further benchmarks on a lot of interesting mobile gpu.
I will be able to do this all for free on many expensive devices 
thx to fantastic support of Open Source projects from wonderfull people at ![](https://p14.zdusercontent.com/attachment/1015988/iWSa0r2vpJa3HJ3VIlARk6jV1?token=eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..Ira7U_VYY-kqDfDa8EkR7g.ZYTZMzKdOzVpYaxAUB2KwkuTx0tgYP78xvtCrscYDszEdg7Rc4Kwn5hbyYE3x1R0imPi1GbfRf_DHG4DEFJ6jnRjFk0634XMcPdy53AXa5KFRGEXmVOC7f8V3wZJoFDZ5hRJ93qB7EjMMyfsysQzbPf49KGpU08mh8rTrCzc6Nm7PlQ6MWIe0VoAKS5CwXGQ8I7MpdDAuOoH25SmQ0_E5C7RzTePaUeGLsZ72abjJK89KP1X9FgAPHyCqtthkzRYbmFinNgWKp4NeLQ5NyfSvdQJo7_Tl-DL5-pwdV_jIko.V5Z-aZfxouelLed3CtdxRA)
