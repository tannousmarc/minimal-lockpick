# Lockpicking JS minigame
Minimal JS game which imitates the mechanism of a safe to 'crack' digits. Spins clockwise/ccw alternatively, hit the digit to proceed.

Positions are randomly generated, spinning is alternative, speed is distance divided by time where the distance is randomly generated.

![Screenshot](https://cloud.githubusercontent.com/assets/6099321/19220570/287bd74a-8e28-11e6-8fe0-4e7e64abdf5e.png)

#Demo
You can see [a fully functional live demo](http://www.tannousmarc.com/projects/lockpicking/index) on my webpage.

If simply watching is not quite your cup of tea, [play with the code instantly in the browser](http://codepen.io/marctannous/details/qONmob/) or fork the project on github.

#Known issues
Initial version, uses jquery and CSS transforms (which are really flawed). Best course of action is changing how the actual game mechanic works.

- CSS considers 3600deg != 360deg but -3600deg == 360deg for some reason. Hence, counter clockwise spinning sometimes caps unexpectedly.
- Because of the same reason as above, sometime speed may be very very small. The way speed is calculated is distance/time with a fixed time animation, but random distance. For a distance of 0deg to -3600deg, CSS might equal it to distance of 0deg to -360deg.
- Tapping on mobile works, but the spacing/sizing is off. 
