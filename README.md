# First shader
This will be my repo to create my own Minecraft shader. I will update it pretty much every day.

I'm not starting from scratch; I'm using this base shader : 

https://github.com/shaderLABS/Shadow-Tutorial?tab=Unlicense-1-ov-file

I'm also watching a tutorial on YouTube to know where to start. The tutorial is made by:

https://www.youtube.com/@timetravelbeard3588

## day 1

Today I learn how to change the color of the screen using the composite.fsh file.

- Firstly, using a basic command :

  float blue_amount = 0.5;
  color = mix(color,vec3(0.,0.,1.),blue_amount);

- then by calling an existing command :

  color = make_green(color, amount);

  while the command was :

    vec3 make_green(in vec3 color, in float amount)
    {
	    color = mix(color,vec3(0.,1.,0.),amount);
	    return color;
    }

  and :

    color = make_green(color, 0.5);

- What I finally came up with :

    I made a Minecraft shader option that we can access inside the game, with which we can change the color of the screen to blue or green. it start a 0, so the game looks normal, but we can change it to 0, 0.25, 0.5, 0.75, and 1. I made them work using a function for the green one and just straight code for the blue one. I also made a function to change not only the screen but the texture, so now I also have a grayscale option, so I can make my game black and white (it also starts at 0 and changes from 0 to 1 like the others). Then I do an en_US.lang file so I can make a custom name and description. Right now, I only do it for the grayscale.

For the next update, I will try to import a picture in this repo so I can show what I'm telling.
