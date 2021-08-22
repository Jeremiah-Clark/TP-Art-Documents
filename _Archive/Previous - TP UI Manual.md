# The Basics

Before getting into any specifics, some basic systems will need to be addressed. 
These exist not to limit creativity but to ensure that what we create is cohesive. 
It also helps to speed work along by removing ambiguity and thus lowering the cognitive load.

### 8-Point Grid

A standard method for laying out a UI is to use an 8pt grid.
This means designing elements in dimensions divisible by 8 (8, 16, 24, 32, 40, 48, etc.), same with the padding (spacing) around elements.
The most important reason for this is that every element is designed to a common standard.
It also cuts down on tinkering and decision making by reducing the number of sizes and spacings available to experiment with.

While any number of standards would work, an 8-point standard is widely used and brings a pleasing (and familiar) feeling to the design.

> **Important**: This is not a hard and fast rule.
> The point is to default to multiples of 8 and to only break the grid with a good reason.

### Sizes and Spacing

It’s a good idea to limit the available sizes and spacings to keep from getting bogged down in decisions of a few pixels.
In this way, you won’t waste time waffling between, for example, a size of 18pt or 20pt.
Instead, you’ll try 16pt and 24pt, pick the one that works best, and move on.

![](20200518%20Size%20and%20Spacing%20@3x.png)

4 8 12 16 24 32 48 64

All of these spacings land on the 8pt grid, except for 4pt and 12pt.
The smallest spacing that should be used is 4pt, though only if really needed.
And 12pt exists because, at smaller sizes, smaller increments are called for.
Most UI elements will be larger than this, with a minimum of 24pt recommended for UI elements, and 32pt for buttons.

> **Important**: Once again, these are not set in stone, but more often than not, one of the sizes above will work well enough, especially early in the design process.
> It’s more important to get good enough and keep moving forward than to get it just right.

### More out than in

Outer margins should be larger than inner margins

### Text

Our default UI fonts are **Triomphe** and **Modulus Pro**.
Our wordmark font is **Gentona Bold**.

#### Triomphe

Triomphe is a clean geometric sans serif font that looks good at a variety of sizes. 
It’s unadorned enough to not draw too much attention to itself but has a less austere, more playful feel than a lot of geometric typefaces. 
It is available in Thin, Light, Regular, Bold, and Black varieties, with Italic variants. 
We typically stick with Regular and occasionally Bold.

Triomphe Regular at a variety of point sizes:
![](20200517%20Text%20Example%20@3x.png)

#### Modulus Pro

Modulus Pro is a rounded geometric sans serif that works particularly well large, but is still readable small. 
It has a casual feel, while still being regular enough to be legible. 
For our purposes, Bold is the variant that works best.

Modulus Pro Bold at a variety of point sizes:
![](20200611%20Text%20Example%20@3x.png)

#### Gentona Bold

Gentona Bold is a condensed geometric font that’s neutral while having just a bit of fun (it’s all about that lower case Y). 
Our word mark is written in this font with no spaces, and all lower case.
(tastypill word mark)

#### Text Size

To avoid choice paralysis once again, text sizes should be limited, at least initially, to the sizes shown in the images above: 
10, 12, 14, 18, 20, 24, 30, 36, 48, and 60.

Text that’s meant to be read should never be less than 10pt. 
A size of 16pt is a good starting point for body text, 24pt for labels, and titles.

> **Important**: It really is best to stick to the sizes above. 
> Too many text sizes in a UI can easily make it look busy and disorganized.

### Buttons

Among the most common elements are buttons. 
In keeping with the 8-point design system, all buttons should be designed in 8pt increments. 
No button should be less than 32pt in its smaller dimension, and anything more than 64pt in height or 176pt in width should be reserved for unique elements.

Default recommended button sizes:
![](20200520%20Button%20Grid%20@3x.png)

#### Round Buttons

Notice that the round buttons specified above are a bit larger than their rectangular counterparts. 
The reason for this is that circles of the same size have less visual weight since they have less area. 
To compensate for this, the circle needs to be made just a bit larger.

The overlap (right) shows how the larger circle has roughly the same surface area as the rectangle:
![](20200518%20Circle%20&%20Square%20@3x.png)

For elements to remain aligned and maintain spacing, the padding around the circle should be reduced to compensate. 
In the image, the 48pt square has 8pt padding all around, while the 52pt circle has 6pt padding, and it is being allowed to intrude 2pt into the square’s padding.

### Touch Area

Apple recommends a minimum touch area of 44x44 points, and it’s a good idea to stick to it when possible (Apple’s own UI designs break this in places, do as they say not as they do). 
To be more precise, a button can be smaller than 44pt, but in those cases, there needs to be enough space in the design to allow for at least a non-overlapping 44x44 point touch area.

For elements as small as 28pt, the standard 8pt of padding will allow for a touch area of 44pt. 
For larger elements, the touch area will dictate the minimum required spacing:
![](20200518%20Touch%20Area%20@3x.png)

> **Important**: As already stated, 32pt is the smallest recommended button size. 
> If you really need to go smaller, 28pt should be considered a hard limit.

## Basics Summary

- Design using an 8pt grid whenever possible
- Limit your options for element size and spacing, and text size, to speed up production
- Triomphe Regular and Modulus Pro are our default fonts
- Gentona Bold is our word mark font, use sparingly!
- Use text sizes no smaller than 10pt
- Try 16pt text for UI elements, 24pt for labels
- Make circular elements slightly larger than rectangular elements, reduce the padding around them to compensate
- Leave enough room for a minimum 44pt x 44pt touch area for anything that the player needs to touch.

# iOS UI Design Requirements

> There are several limitations and constraints that we have to keep in mind when designing UI for iPhones. 
> The most fundamental restriction we work with involves the dimensions of iPhone screens. 
> This can be a bit daunting at first, so let’s start with the most basic units at work.

### Points vs Pixels

At first, this was simple, Pixels were all you had to worry about because Points were the same as Pixels.
Then Apple started making phones with different screen sizes, so they implemented a system that uses Points for design, and Pixels for display. 
They did this so that even as their screens’ Pixel dimensions got larger, their Point dimensions stayed relatively similar.

The idea is to design layouts and UI elements in points, and export at x1, x2, and x3 to cover all different iPhone models. 
That means that a UI element designed at 50pt will be exported at 50px, 100px, and 150px. 
One of those three sizes will be appropriate for any iPhone currently in use.

> **Important**: Going forward, unless otherwise noted, all dimensions given should be assumed to be in Points, not Pixels.

## iPhone Screen Specs (X and newer)

**iPhone X, Xs, and 11 Pro (scale x3)**

- Design dimensions: 375 x 812 points
- Display dimensions: 1125 x 2436 pixels

**iPhone Xs Max, and 11 Pro Max (scale x3)**

- Design dimensions: 414 x 896 points
- Display dimensions: 1242 x 2688 pixels

**iPhone 11 and XR (scale x2)**

- Design dimensions: 414 x 896 points
- Display dimensions: 828 x 1792 pixels

### The “Notch”, and Corners

The iPhones X, and newer models, have a “notch” at the top of the screen that contains the front-facing camera and other sensors. 
This Notch extends 30pt down and is 209pt wide. 
The corners are also rounded on these phones, unlike previous models. 
The corner radius is 40pt, meaning that the curve extends 40pt along each edge.

Both the Notch and the screen corners reduce the useable space of the screen, and being physical characteristics of the hardware are always present.

Detail of the "Notch" and top corners with point dimensions.
![](20200515%20Notch%20and%20Corners%20@3x.png)

### Home Bar

Finally, there’s the Home Bar, which is about 13pt from the bottom of the screen (I couldn’t find this officially spelled out anywhere, so I measured this myself from screen grabs). 
Unlike the Notch, the Home Bar is a graphical element, but it should be treated as physical since it is nearly always visible.

Detail of the Home Bar with approximate point dimensions.
![](20200515%20Home%20Bar%20@3x.png)

## Target: iPhone X (and Xs, 11 Pro)

In practical terms, the iPhone X point dimensions are the most sensible to use. 
A 375pt wide design will fit on a 414pt wide screen without scaling, by just adding a little padding either between objects or to the sides of the screen.

### Safe Area

Apple recommends keeping important content 44pt from the top of the screen (14pt below the Notch), 34pt from the bottom of the screen, and 16pt from the sides.

The top area applies more to apps than games, to leave room for the system bar at the top. 
Since games cover this, it's less of a concern for us. 
The bottom margin is meant to avoid interfering with the Home Bar, which does remain visible in games, but the margin is still a bit bigger than it needs to be.

With this in mind, we can safely reduce the top margin by 12pt, and the bottom margin by 18pt.

Apple's recommended Safe Area compared to our expanded Safe Area.
![](20200515%20iPhone%20X%20Specs%20@3x.png)

This makes our Safe Area 343pt x 764pt. Width-wise, these will also fit on the screens of the iPhone 8 and 7, though those are proportionally shorter.

A visual comparison of our Safe Area with various screen sizes.
![](20200518%20iPhone%20X,%20Max%20Specs,%20Safe%20Area%20@3x.png)

#### Full Span Elements

Any element that spans the full height or width of the screen needs to be designed for the larger phones so it doesn't need to be scaled (ideally, no elements should ever be scaled, though in reality that’s unlikely). 
That means that full width elements should be 414pt wide, and full height elements should be 896pt tall. 
The important parts still need to fall within the iPhone X dimensions.

A cropped of an example UI design showing spacing, and how a full span element needs to be made wider than the target screen.
![](CleanShot%202020-05-15%20at%2014.32.33%20Cropped.png)

## iOS Design Summary

- Points and pixels are not the same. Design in Points, then export at x3 pixels to ensure compatibility with modern iOS devices
- **Safe Area** → 343pt x 764pt
- **Target Screen Size** → 375pt x 812pt
- **Maximum Screen Size** → 414pt x 896pt
- Keep anything of importance within the **Safe Area**
- Ensure that any full-width elements account for the **Maximum Screen Size** to avoid scaling

# Wireframes & Storyboards

> Wireframes are a low-fidelity way to explore and communicate the workings of a game without putting too much time into it upfront.

> A storyboard might be best described as a comic strip, showing moment to moment interactions and events. 
> Often the same screens can be used for both Wireframes and Storyboards, which is why they are lumped together in this section.

## Why Wireframe?

The point of a wireframe is to show how a player will interact with a game by showing available actions and their results. 
By following the arrows, you should be able to get a good idea of the flow of play, and hopefully, of any required changes or omissions.

Structurally, wireframes consist of screen mockups that are connected by arrows and other labeling to indicate the flow of interactions.

#### Wireframe to Final UI

Depending on the level of detail, and how closely the wireframe represents the final design, it may be quicker and easier to refine a wireframe into a final UI design. 
Don’t depend on that, however, and don’t add unnecessary detail with that expectation. 
It is the fate, and purpose, of most wireframes to be discarded once they have served their purpose.

![An example of a wireframe (uses an older template, will update at some point).](WFH%20Overview%20Flow%20copy.png)

## Why Storyboard?

Where a Wireframe shows the overall user flow as a player navigates through a game, a storyboard can display a single scene, mechanic, or interaction in greater detail, and in a linear way. 
It is often necessary to supplement the screen images with narrative or descriptive text.

![An example of a storyboarded interaction (uses older version of the symbol library, will update).](Scene%20-%20Texting.png)

> **Important**: For the rest of this section, unless stated otherwise, it is safe to assume that everything applies to both wireframing and storyboarding.

## General Details

### Color Definitions

For a wireframe, colors and shapes should be kept to a minimum. 
This is to ensure clarity and a focus on the functional design rather than aesthetics.

For the sake of consistency, only these colors and patterns will be used in wireframes:

![](20200519%20Wireframe%20Colors%20@3x.png)

### Buttons

Buttons are reasonably self-explanatory, they are any UI element that is “pressed” to cause something to happen.

![](20200520%20Buttons%20@3x.png)

- **Fill**: White
- **Outline**: Dark Gray, 2pt, Inside
- **Text**: Triomphe 12pt to 36pt (depending), Medium Gray
- **Symbol**: Don’t bother with symbols for Wireframes, unless there’s already one made that you can use, or it’s somehow essential. Even then, keep it simple (my template includes a basic star, diamond, arrow, shield, gear, and dollar sign).

### Other Game Elements

Anything else that is needed to demonstrate gameplay and user flow can be constructed from basic shapes. 
Since it’s impossible to predict all of the variety that may be needed, here are some general guidelines to follow:

- Build only what is needed to get the point across
- For interactive elements use a Dark Gray outline, 2pt thick, with a White fill
- For non-interactive elements use a Medium Gray outline, 1pt thick, with an Off-White fill
- In-game text and labels on light backgrounds are Medium Gray
- In-game text and labels on dark backgrounds are Off-White

### Labeling

Labeling isn’t part of the game, it is there to label and identify what you are looking at. 
There are three types of labeling in wireframes, identified by color:

- **Default**
    - Color: Medium Gray
- **Player**
    - Used to identify player actions/interactions
    - Color: Cyan
- **System**
    - Used to identify system/automatic actions
    - Color: Magenta

#### Callouts

Callouts are direct labels of the elements of a wireframe. 
Callouts consist of an arrow and text.

![](20200518%20Callouts%20@3x.png)

- **Arrow**: 2pt, triangle arrow
- **Text**: Triomphe 14pt, 2pt White outline

#### Touches

Touches are used to identify a tap or touch by the player. 
There are four types of touch indicators:

![](20200519%20Touch%20Symbols%20@3x.png)

- **General**: This looks more or less like a bullseye, and indicates a touch and hold that is not specific. This symbol is specifically based on the 44pt Touch Area
- **Targeted**: This has a crosshair, and is used to indicate touching a specific place. This symbol is also based on the 44pt Touch Area
- **Button Press**: These are used to outline buttons that are pressed
- **Infinity**: Used to indicate that the player needs to touch and hold, and move around in various directions
    Touches share these features:
- **Outline**: White 2pt, Cyan 4pt
- **Fill**: None

#### Notes

Notes are used to give further information and context or to provide feedback on a design.

![](20200518%20Notes%20@3x.png)

- **Pin**: Used to indicate that there is a note elsewhere about whatever has been pinned, using the letter/number as a reference
    - Text: White
    - Fill: Medium Gray
- **Post-It Note**: Notes that supply information out of context, usually by indicating a pin for context
    - Text: Black
    - Outline: Black, 1pt
    - Fill: White
- **Info Boxes**: An in-context note, the tail pointing to what is being talked about. Text is Black, fill is White
    - Text: Black
    - Outline: Black, 1pt
    - Fill: White
- **Dimension**: Used to specify sizes of objects and spacing
    - Lines: Red, 1pt
    - Text: White

#### Interactions

Indication of how the player should interact with the game, beyond simple touches and holds.

![](20200518%20Hands%20&%20Arrows%20@3x.png)

- **Arrows**: Arrows show how objects move, or the direction of gestures needed to use
- **Hands**: These hand symbols are to be used when an explicit reference to the player’s hands, or to indicate in-game hands

#### Drop/Target Area

This symbol is used to indicate a target area, or a drop area, for an interaction. 
For example, if an object needs to be moved to a specific spot to trigger an event.
![](20200518%20Target%20Area%20@3x.png)

- **Outline**: Magenta and White dashed, 4pt
- **Fill**: None

### Flow

When constructing storyboards and flow diagrams, these arrows are used to show how actions and elements connect.

![](20200519%20Flow%20Arrows%20@3x.png)

- **Arrow**: A simple, stubby arrow used to show direct movement from one screen to the next in a Storyboard
- **Path Arrow**: These arrows are used in flow charts. They come in three parts to allow for great flexibility (in use these would be butted up against each other to look like a continuous object)
- **Direct Arrow**: This triangle is meant to show that the connected screen is a variant of the current screen, rather than the next screen in a process

## Wireframe Template

Starting with a template makes all of this much easier and quicker. 
It allows for more detailed, more consistent building blocks with little to no extra work, once the template is set up.

### Figma

I’ve built a template in Figma ([Figma.com](http://www.figma.com)), which is a browser-based collaborative vector design program made specifically for UI work. 
Being browser-based means that it is available for any platform with modern browser support, and there is also a downloadable desktop version (which I personally prefer).

The free level includes collaboration (up to two people working on a single file simultaneously), sharing online, and per-file template libraries. 
The paid versions allow for shared libraries and other features.

### Components

![All of the components currently in the library and ready to be used.](20200520%20Wireframe%20Kit%20@3x.png)

Figma refers to the individual items within a library as Components (some other programs call these Symbols). 
Components have several attributes that make them very useful for wireframing and UI work:

- Components are inserted into documents as instances, meaning that updating the master component will update all instances automatically
- Components have overrides, meaning that you can change the scale, colors, and so on and those changes will remain even if the master is updated (unless explicitly reverted)
- Text is always editable
- Anything can be made into a Component, and Components can be nested, which for example means that screens can be built from Components, then turned into Components themselves for assembly into Storyboards

#### Component Library

The library I’ve created has the following categories (which largely mirror the sections detailed above):

- **Buttons**: Buttons, clearly
- **Elements**: A category for all other game elements that aren’t buttons, symbols, or text
- **Flow**: Used for laying out and detailing flow charts and storyboards
- **Interactions**: Show how items in the game are interacted with
- **Notes**: Meta content, description, and feedback items
- **Symbols**: A simple set of symbols meant to identify items in the UI
- **Text**: Ready to go text labels organized by size
- **Touches**: Indicate direct interactions by the player

#### The iPhone X

Of particular note is an accurate iPhone X screen layout, to be used as a base to build on top of. 
The Dark Gray is out of bounds, the Light Gray is outside of the Safe Area, and the White rectangle is the Safe Area.

![iPhone X, Xs, and 11 Pro](iPhone%20X%20@1x.png)

#### Styles

![A few of the styles I've set up in Figma.](20200525%20Styles%20@3x.png)

Figma also uses styles for things like fonts, colors, effects, and even layout grids. 
Like components, a master style can be updated, and anything that uses that style will be updated.

# Final UI

By necessity, a discussion of final UI design needs to be more general, and less prescriptive. 
This section doesn’t focus on rules, but guidelines. Unless otherwise noted, nothing here is absolute.

> **Note**: The spacing, size, and placement rules for wireframes still apply to the final UI design. 
> The 8-point grid, the restrictions on button sizes, spacing, and text sizes are all good to be kept in mind when designing.

## Color

Color is a deep and complicated subject, and different for every game. 
That said, here are some guidelines to follow.

> **Important**: The color guidelines presented here are NOT rules, they are meant to get you on the right track as quickly as possible.

### No True Black, Use White Sparingly

Pure black doesn’t look good on a UI, it’s best to just never use it. 
Instead, use a dark gray, possibly with just a hint of a color (maybe 2-3%) to make it an “Almost Black”.

White isn’t as bad in UI as black, but it stands out so much that it should be used with intention. 
If you simply want an area with no color, use an “Almost White” instead, which will achieve a more harmonious result. 
Save true white for the most important items.

### Start with a Basic Color Scheme

The first thing you should do is pick a few main colors to work with. 
These can be divided into a few categories by use.

#### Primary Color

_You will need at around 5-10 shades of your primary color._
The first color decision to make is the primary UI color. 
The primary color informs the rest of the color decisions, and dictates the feel of the UI As an example, Facebook’s UI is blue, even though the majority of the screen isn’t obviously blue.

Since we’re making fun, casual games, this color should be bright and saturated. 
Our pre-made color palettes (see below) are organized according to bold colors for this reason.

> **Important**: While it’s possible to choose more than one primary color, do so carefully. It’s usually best to have one primary, and a strong accent rather than two primaries.
>
> The primary color will be used on buttons, and other key elements, particularly interactive elements.

#### Accent Color(s)

Nearly as important to the look and feel of a UI is the accent color. 
The accent should be chosen in relation to the primary color, depending on the look you’re going for.

##### Selecting an Accent Color

_You will probably need 5-10 shades of each accent color._
Accent colors are used for highlighting important information, or simply for decoration. 
Two or three Accent colors are often used for different purposes.

There’s a simple trick for making any accent color work with your primary color, or at least for getting close. 
It’s all about balancing the saturation. 
To start with, picture the classic RYB color wheel. 
This is the paint mixing wheel that most of us learn about as children. 
It uses Red, Yellow, and Blue as primaries. 
This color wheel is generally better for color matching than the more common (in digital art) RGB color wheel.

The further away from your primary color your accent color is, the lower the saturation needs to be. 
As a shortcut for this, if the accent color is on the opposite side of the color wheel desaturate it to 25%, if it’s at a 90 degree angle desaturate it 50%.

![](20200526%20RYB%20Color%20Matching%20@3x.png)

This is only a rough approximation, but it’ll get you in the right ballpark quickly. 
These color wheels show the resulting colors with adjustments to the brightness to keep the relative tone intact:

![The color blocks show how profound an effect this can have. The blocks on top start from a fully saturated version on the far left for comparison. The blocks on the bottom show how you can determine a scheme starting from a primary color.](20200526%20RYB%20Color%20Matching%202%20@3x.png)

This is why our color palettes are structured the way they are (see below), to make this process even quicker and easier.

#### Neutral Color(s)

_You will likely need 5-10 neutral shades._
Most of the time neutral colors will be gray. 
Since a true gray can be boring, it’s often a good idea to put just a bit of color into your grays, typically your color scheme’s primary color.

Neutral colors are usually used on the background, popups, modals, and so on. 
Generally, containers and anything that doesn’t need to draw attention to itself. 
When in doubt, these are the lightest and darkest grays currently used in iOS. 
They have just a hint of blue, but tend to look good in nearly any situation.

![](20200522%20iOS%20Black%20and%20White%20@3x.png)

### Color Palettes

The easiest way to speed up the choosing of colors is to start with pre-made color palettes. 
I’ve put together a number of color palettes (with more to come) that can be found at the end of this document.

All of these palettes use the same format:

![The base color includes both a hex code and its Hue, Saturation, and Brightness breakdown.](20200525%20Color%20Palette%20Diagram%20@3x.png)

#### 1st Row - Full Saturation

The top row of colors is the most saturated. 
The tall color (usually in the middle) is the base color for the palette, the one used to generate the rest of the colors. It is the tallest in order to make it quick to reference.

#### 2nd Row - 50% Saturation

The second row is desaturated 50%, with some adjustments in lightness to keep roughly the same relative tone.

#### 3rd Row - 25% Saturation

The third row has the saturation halved again to 25%, again with slight adjustments to brightness.

#### Grays - 0 Saturation

These are grays that match the colors above them in value. 
This row is boxed off since it’s really not a part of the color palette, but does offer a way to judge each column’s relative value.

#### Almost Black and Almost White

These are on every palette for easy reference. Eac

## Buttons

Buttons are the arguably most prominent UI elements in terms of their impact on the look and feel of a game. 
If nothing else, buttons need to be clear and communicative at a glance.

A typical casual game button will have an outline, a background color, and a text label, a symbol, or often both.

### Colors

It is best to keep all of the colors of a single button monochromatic. 
Once a primary color has been chosen for a button, for example dark blue, then all parts of the button (background, outline, text, and symbol) should be colored using the dark blue color palette.

![A variety monochromatic blue buttons with strictly gray versions below each (which is a good way to compare).](20200524%20Button%20Examples%20-%20Colors%20@3x.png)

#### Using Black and White

You can use black and white for the text (and any symbol) if you want to draw attention to it. 
Even in these cases it may be better to use Almost Black and Almost White. 
The difference is slight, but it gives a more harmonious result.

![](20200525%20Colors%20on%20Buttons%20@3x.png)

### Outline

A 2pt outline is a good place to start, it especially looks good with smaller buttons. 
It is more important to keep the outlines between buttons consistent, and to only vary them with purpose.

![Depending on circumstance, different outline widths may look better at different sizes.](20200525%20Button%20Examples%20-%20Outlines%20@3x.png)

### Corners

Giving buttons rounded corners makes them appear more friendly, and is typical for casual game UIs. 
A corner radius of 6pt is a good starting point. 
This might need to be enlarged for very large buttons, but for the most part 6pt is as small as you should go. 
And, as always, stay consistent without a good reason not to.

![Depending on circumstance, different corner radii may look better at different sizes.](20200525%20Button%20Examples%20-%20Corner%20Radius%20@3x.png)

A large enough corner radius will result in a pill shape, which creates a different feeling altogether.

### Labels

All of the buttons shown so far have had labels. 
We already have preferred fonts to use (Triomphe and Modulus Pro, the choice is dependent on the rest of the text in the game), so that leaves placement and size.

#### Label Placement

TO DO

![](20200525%20Text%20Baseline%20Alignment%20@3x.png)

#### Label Size

When in doubt, leave more open space around a label, rather than less.

TO DO

### Symbol

It’s often a good idea to include a symbol on a button to draw attention, or to make it quicker and easier to identify what it does. 
Typical symbols include arrows, stars, monetary symbols, locks, swords, shields, and so on.

#### Symbol Design and Placement

The important thing with these symbols is that they be simple shapes with strong silhouettes. 
In most cases it is best to make a symbol only a silhouette, since they’re usually fairly small on screen and too many details will just get lost.

As for placement, there are many options:

![There are nearly limitless ways to apply a symbol to a button.](20200611%20Button%20Symbol%20Positions%201%20@3x.png)

The upper left example is the most basic, and when in doubt will work in nearly every case, but don't be afraid to experiment.

As with most things in UI design, consistency is key. If you decide on very simple shapes, make sure all of your button symbols are equally simple.

#### Symbol Size

If the button includes a text label, it is important to ensure that the symbol is sized to work with the text.

TO DO

![](20200525%20Button%20Symbol%20Positions%202%20@3x.png)

When in doubt, leave more space rather than less around a symbol

#### Horizontal Spacing

TO DO

#### Vertical Centering

It might seem like this is simple, that symbols should simply be vertically centered. 
With a regular, symmetrical symbol, that works fine. 
Many symbols will have an off-center visual weight, and will need to be shifted slightly away from that center slightly in order to feel properly centered. 
For example, the pointed end of a fat arrow has less visual weight than the blunt end, so it should be shifted a pixel or two towards to pointed end.

![Examples of symbols and how I would shift them vertically.](20200525%20Button%20Symbol%20Positions%203%20@3x.png)

It’s a small change, but leads to a more refined look.  

With some symbols it’s possible to take this to extremes. 
For example, a padlock icon. 
In these cases you can treat the bulk of the symbol as the entire symbol, and leave the rest overlapping:

![](20200525%20Button%20Symbol%20Positions%204%20@3x.png)

It is important to take into account the space taken up by the symbol so that it doesn’t overlap or intrude on other elements accidentally.

### Button States

Buttons generally exist in one of several states:

- **Inactive** - In this state the button can not be pressed.
- **Normal** - The buttons is active and can be pressed.
- **Pressed** - This transitory state communicates that the button has been pressed.
    In general, inactive buttons should be at the very least desaturated, and possibly also lighter. 
	Pressed buttons should be darker and have less contrast.
    ![An example button showing one way to indicate states.](20200525%20Button%20States%20@3x.png)

## Modals and Popups

TO DO

# Game Art Folder Structure

## Game Art Assets

### Assets

- **View**: Dev, Production
- **Edit**: Art

### Documents

- **View**: Dev, Production
- **Edit**: Art

## Library

- **View**: Dev
- **Edit**: Art, Production

- The Library contains assets of all types that are available to be used in projects. This includes purchased assets as well as custom made.
- Assets created or altered in-house will have “-TP” appended to the file/folder name.
- If more than one version of an asset or plugin is needed, the older or alternate versions should be placed in a labelled sub folder.

- For example, the current version of the Minimalist shader is in the Shaders folder, while the previous version*(\_needed for older releases of Unity) is in a sub folder called “Minimalist Shader - Old Version”*.\_

### Screenshots

- **View**: Dev, Production
- **Edit**: Art

- When sharing screenshots, it can be helpful to put them here to create a visual record of development.
- This isn’t required, and we’ll see if it even proves useful.

### Working

- **Edit**: Art

- The Working Folder contains all of the work done for our projects, organized into folders by project (with“date-project” naming).
- This folder should only ever be accessed by the people doing the work, and **all current work** should be saved in this folder.

# File Naming & Organization

## Definitions

First, let's make sure we all know what the following terms mean in this document.

- **Working File** \- Working files are the source files native to our authoring programs. For example, PSD files for Photoshop and LXO files for Modo. These files are only of use to the art team and should not be included with final files sent to developers unless specifically requested.
- **Final File** \- These are the files that are sent along to the next stage of development. Typical examples include PNGs for textures and FBXs for meshes.
- **Working Folder** \- Each project should have only one master folder that contains all related materials and files, including final files, documents, references, and working files.
- **Assets Folder** \- Each project also has an Assets Folder, which contains everything the Project Folder does, except for working files. This is where devs can look for the most recent final files and other project-related materials.
- **Sub-Folder** \- Any Folder within the Project or Assets Folders.

---

## Naming Conventions

### Project & Asset Folders

**Name Format:** _YYYYMMDD-\[Project Name\]_

- **YYYY** \- The year, all four digits
- **MM** \- The month as a two-digit number
- **DD** \- The day as a two-digit number
- **Project Name** \- The working title of the project

### Working Files

**Name Format:** _YYYYMMDD-\[asset type\]-\[asset name\]-\[suffix\].ext_

- **YYYY** \- The year, all four digits
- **MM** \- The month as a two-digit number
- **DD** \- The day as a two-digit number
- **Asset Type** \- Asset types can be specified, especially when different assets share a file type (for example, multiple PSDs with different purposes).

- For example:

- Mat (material)
- Tex (texture)
- Storyboard
- Doc (game document)
- UI

- **Asset_Name** \- Simply the name of the asset, using whatever descriptor will make it most clear.
- **Suffix** \- Sometimes, an additional identifier is needed to distinguish variations. Some asset types, like texture maps, have specific suffixes (BaseColor, Normal, Roughness, etc.).
- **ext** \- The file extension
- **Spaces are ok** \- With working files, spaces are permissible in the file name. CamelCase should be used for words that are not spaced. Dashes should be used between the various parts of the name.

- NOTE: Dashes are used because double-clicking within a file name will select all characters between dashes, making editing file names easier.

### Examples

- Tex-DarkWood.psd
- Tree House.FBX
- UI-Start Screen.afdesign

---

## Final Files

**Name Format:** _\[asset_type\]-\[asset_name\]-\[suffix\]-\[version\].ext_

- **Asset_Type** \- Asset types can be specified, especially when different assets share a file type (for example multiple PSDs with different purposes).

- For example:

- Mat (material)
- Tex (texture)
- Storyboard
- Doc (game document)
- UI

- **Asset_Name** \- Simply the name of the asset, using whatever descriptor will make it most clear.
- **Suffix** \- Sometimes a further identifier is needed to distinguish variations. Some asset types, like texture maps, have specific suffixes.

- BaseColor
- Roughness
- Normal

- **Version** \- If necessary, a version number can be added to the end of the file name. It's a good idea to use a two digit number from the beginning, starting with 01.
- **ext** \- The file extension
- **No Spaces** \- Final file names should _not_ include spaces. An underscore can be inserted in place of a space. CamelCase can be used for words that are not separated by an underscore. Dashes should be used between the various parts of the name.

- NOTE: Dashes are used because double-clicking within a file name will select all characters between dashes, making editing file names easier.

### Examples

- Tex-DarkWood-Normal-02.png
- Tree_House-Large.fbx
- UI-Button-Start-Active.svg

---

## Folder Organization

### Working Folder

All work should be done in the Working Folder, and the Working Folder is considered the master version of the project assets.

- NOTE: It’s a good idea to set up an automation to keep the Working and Asset Folders in sync. The sync should be one way, from the Working Folder to the Asset Folder, and should skip all working files.

**Sub-Folders** \- Project folders should contain at least these standard sub-folders.

- **\_Meshes** \- For new and custom meshes.
- **\_Textures** \- For new and custom textures and materials.
- **Archive** \- Don't throw things away, instead move them to the archive folder. The other sub-folders may contain their own Archive folders.
- **Documents** \- Any documents related to the project, including game docs, storyboards, flow charts, and so on.
- **Existing** \- This is for pre-existing assets, whether from previous projects or purchased assets. If you are going to make changes, or use them for reference, put them in this folder so that the original is preserved.
- **Reference** \- Anything that you collect as reference material goes in here.
- **Screenshots** \- You'll take many screenshots as you work, to show things to people. It's also a good idea to take screenshots regularly to track progress. Put them in here to keep the folder uncluttered.

- NOTE: An underscore at the beginning of a folder name will cause that folder to sort to the top.

### Asset Folder

All work should be done in the Working Folder, NOT THE ASSET FOLDER. 
The Asset Folders exists to make finding Assets easier, and to keep the working version of the project isolated from anyone who doesn't need to make changes to it.

The sub-folder organization of the Asset Folders is the same as the Working Folders, because it is synced from there.

---

## Unity Project Organization

### Custom Assets Folder

All art assets imported into Unity should go inside a folder called “Custom Assets”. 
The Custom Assets folder should include these sub-folders:

- **Materials** \- Texture maps and materials. Be sure to use the following asset type prefixes
- **Meshes** \- 3D models
- **Prefabs** \- All prefabs, whether made from custom assets or variants of existing prefabs
- **Scenes** \- Any scenes you set up
- **Scripts** \- Custom scripts and related files (this usually for developers, not artists)
