# Raytracing

Online raytracing tutorial using Shadertoy.

This tutorial is heavily based upon []() and [](). 
It's goal is to have a working raytracer in a minimum of steps.

But rather than doing it offline with c++, I focus on doing it in a webbrowser, using [Shadertoy]().
It has the benefit of making it very interactive, simpler and faster (realtime) because of the use of shader.
And somewhat bit more complicated for complete beginer because of some shadertoy Magic. I let you judge (by refering yourself to the original tutorial). 

This tutorial (I made for myself) follow the same plan than the one I am referring to.


## Step 1: Generate an image

When creating a new shader on Shadertoy, we get some sample code which is close to the following one. Which is made to get the exact same rendering than in other tutorial.

{% highlight cpp %}
void mainImage( out vec4 fragColor, in vec2 fragCoord )
{
    // Normalized pixel coordinates (from 0 to 1)
    vec2 uv = fragCoord/iResolution.xy;

    // Time varying pixel color
    vec3 col = vec3( 1.0 - uv.y , uv.x, 0);

    // Output to screen
    fragColor = vec4(col,1.0);
}
{% endhighlight %}

_mainImage_  is the equivalent of the render function. It's job is to output for a given screen coordinate an color for this pixel. It uses normalzed coordinates (between 0 and 1). And produce the following output:

<iframe width="640" height="360" frameborder="0" src="https://www.shadertoy.com/embed/ts2GRh?gui=true&t=10&paused=true&muted=false" allowfullscreen></iframe>


