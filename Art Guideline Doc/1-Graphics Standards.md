## Graphics Standards

### COLORS

The colors you choose should be fun, comfortable, and inviting.
Colors that are too aggressive, or that clash, will drive players away.

**Improving Colors:**

![](_attachments/color%20improvement.png)

##### Forbidden Colors

![](_attachments/black_and_white.png)

Pure black and pure white should be used sparingly graphics, except in UI graphics.
Even then, use sparingly, and mostly for emphasis.

### SHAPE LANGUAGE

Second only to color is shape language.
This is the simplest and most universally understood example of shape language:

![](_attachments/shape_language.png)

**Once your shape language is defined, stick to it.**

### CONTRAST

Contrast identifies points of interest, and separates active and passive elements.
Too much contrast can be unpleasant, too little is difficult to read.
Whether the light colors are surrounded by dark, or the dark surrounded by light, also has an impact on what is communicated.

![](_attachments/contrast_colors.png)

These are only guidelines, **most important is to make your game readable.**

#### The B&W Test

This is a quick and easy way to test the contrast in your game.
Take a screenshot or render and make it black and white.
Study how distinct and readable objects are, especially against their backgrounds.

![](_attachments/b&w_test.png)

### SHADERS

**Don’t use the Unity Standard Shader.**
A toon or unlit shader will work better in most instances.

![](_attachments/shader.png)

- **MK Toon**: A relatively light weight toon shader with a number of interesting stylization and lighting options
- **Toony Colors Pro 2**: More complicated but with more features and flexibility than MK Toon


### LIGHTING & SHADOWS

Lights and shadows must be used carefully if they are used at all.

#### Performance

Toon shaders do not react to lights in the usual way, but shadows still impact performance.
If you have a complicated or detailed scene with performance problems, try turning shadows off for some objects, maybe all of them.
Unlit shaders with no shadows can look flat and lifeless, so do this strategically.

#### Lights

The only real light sources in a scene should be a directional light (included in a new scene by default), and the skybox or ambient light.
The directional light will control the direction and strength of shadows.
The skybox is best used to impact the color and feeling of the scene.

![](_attachments/light_and_shadows.png)

Only add more light sources if absolutely necessary, and test to be sure they do not impact performance too negatively.

#### Shadows

![](_attachments/shadow_opacity.png)
