# Shader Project

This is my repo for creating my own Minecraft shader. I will update it pretty much every day.

I'm not starting from scratch; I'm using this base shader:

https://github.com/shaderLABS/Shadow-Tutorial?tab=Unlicense-1-ov-file

I'm also following a tutorial on YouTube to know where to start. The tutorial is made by:

https://www.youtube.com/@timetravelbeard3588

## Day 1

Today I learned how to change the color of the screen using the `composite.fsh` file.

- First, using a basic command:

  ```glsl
  float blue_amount = 0.5;
  color = mix(color, vec3(0., 0., 1.), blue_amount);
  ```

- Then by calling a function:

  ```glsl
  color = make_green(color, amount);
  ```

  where the function was:

  ```glsl
  vec3 make_green(in vec3 color, in float amount)
  {
      color = mix(color, vec3(0., 1., 0.), amount);
      return color;
  }
  ```

  and:

  ```glsl
  color = make_green(color, 0.5);
  ```

- What I finally came up with:

    I made a Minecraft shader option that can be accessed in-game, allowing the player to change the color of the screen to blue or green. It starts at 0, so the game looks normal, but it can be changed to 0, 0.25, 0.5, 0.75, or 1. I made them work using a function for the green one and inline code for the blue one. I also made a function to change not only the screen color but the texture as well, so now I also have a grayscale option to make the game black and white (it also starts at 0 and goes up to 1 like the others). Then I created an `en_US.lang` file so I could set custom names and descriptions. Right now, I've only done it for the grayscale.

- Options:
	![Options](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20002903.png)

- Default game colors:
	![Default](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20003135.png)

- With blue at 0.5:
	![Blue 0.5](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20003031.png)

- With green at 0.5:
	![Green 0.5](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20003016.png)

- With grayscale at 1:
	![Grayscale 1](https://github.com/okalypto/shader-day-1/blob/34b741099eded7d85797425f9f9b664c491fcc0e/Capture%20d'%C3%A9cran%202026-03-17%20003117.png)
