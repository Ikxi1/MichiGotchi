# EXTREMELY WIP

## 🎮 Chievee Desktop Pet

### 💻 Gameplay

- Being a desktop pet, Chievee will need to have different "states" (idle, walking, etc...) each with their own assets, animations and set of rules.
	- All states are toggleable by the user and the frequency of occurrence is also adjustable
	- Idle - just standing there, menacingly, looking at the computer user
	- Sitting - just sitting around, swinging her legs
	- Sleeping - just sleeping whereever she wants to
	- Walking - left or right
	- Yapping - she gets bigger, blocks the screen view and just starts yapping (not yet fully thought out, if it will just play sound bites or what)
- Besides Chievee, will other character make an appearance? Which one(s) and for what purpose?
	- Depending on time and budget constraints, mostly time
	- Probably Jared, because chat might want it
	- ~~Other VShojo members (and Mata)~~
	- Her friends
	- They'd be causing mischief with her, or other interactions, tbd
- What are the different possible situations the user may be able to interact with Chievee, and how?
	- Clicking on her and dragging her to different parts of the screen
		- She can be positioned at any position on the screen (on top of an in-game minimap for example (the program won't know any of the UI elements of other software or the OS, it will just know where you dropped Chievee))
	- Making her eat/drink
- How does the game communicates information and feedback to the user?
	- All information will be shown as "actions by Chievee"
		- If she feels lonely, it will show a thought bubble of her friends
		- Same with food and water (if she actually thinks of those)
- She can also be an alarm clock
	- Set her to go off "in 30 minutes" or "at 1500"
	- Alarm sounds could be taken from her sound board or just ask on stream "hey could you make some alarm clock noises" (don't think that would give her any hints)


🎨 **Assets**

- General art direction:
	- Needs more thought
	- Pixel art would need to be higher detail and thus quite a bit more effort, otherwise the individual pixels would be too big on screen
	- Vector art (I'm thinking Scribblenauts) could work and animations would be too hard to do (wouldn't have to redraw every frame)
	- Traditional 2d animation might work, but would take a lot of time (even low framerate)
	- 3d would also work, though we'd need a fully textured and rigged model and style would then also be important
- Chievee: how many assets and animations will we need?
	- If it's pixel art,
		- we can do simple spritesheets for all the actions, or just one large sheet. I would probably have 4-6 frames per animation, that would have enough detail but also cut down on work.
		- The other assets could also be put on one large sprite sheet.
		- The UI could also be handled like a sprite sheet
	- If it's vector art
		- we can also do sprite sheets or just use SVG files and then animate them in engine cutting down on animation work.
		- Other assets would be in each of their SVG files
		- UI could be easily scaled
	- If it's traditional 2d animation
		- we'd do the same as for pixel art
	- If it's 3d
		- we'd need a full model with textures, rigging, animation
		- Other asset modelled and textured (or CC0 licensed)
		- A shader to make everything look the same style
- What sound effects may we need?
	- I don't think SFX are necessary, as it would be more distracting from other things, unless a user really wants some focus like with Chievee
- Which UI elements will we need? What will be the (rough) layout?
	- Just a small box with some buttons

🔧 **Other/Technicals**

- How are the game mechanics explained to the player?
	- As it won't be that complex, I don't think much explanation needs to be done. There can be a README.txt that would just explain, "left-click on chievee to do stuff" "right-click on chievee for a menu" and "left-click drag chievee to position her where you want"
- Do we want English only or multi-language? For the latter, what elements would need to be translated?
- What are the important options to keep in mind? (Window size, sound volume, ...)
	- A mode that would allow "complete mouse passthrough", so Chievee does not get in the way. Difficulty: Figuring out how to exit the "complete mouse passthrough", as you cannot click on the program anymore.
- What about accessibility features? (colorblind mode, ...)
	- Colourblind shouldn't be too hard (https://github.com/paulloz/godot-colorblindness)
- How will the save system work?
	- There is just a settings file that everything will be saved to. Chievee's last position will not be recorded, as it could mess up when the user changes the amount of screens they have (she could land outside the visible area)