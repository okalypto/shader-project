# Shader project
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

- options :
	![Image Alt](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20002903.png)

- basic game color :
	![Image Alt](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20003135.png)

- with blue at 0.5 :
	![Image Alt](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20003031.png)

- with green at 0.5 :
	![Image Alt](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20003016.png)

- with grayscale at 1 :
	![Image Alt](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20003117.png)

## day 2

Today I learn where is what, for example, the terrain is separeted with the entities and everything else. With this, I can now change colors on a single part of the game (not on the whole screen like in composite).

I also learn how to make a file give info to others (or some kind), so I can make a function in a file and use it in another one.

I learn how to change the color of the sky, clouds, entities, terrain, and sun (moon two). I also made a grayscale that only acts in terrain, so I can make entities red and land gray.
