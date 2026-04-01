## Simple Circular UI Layout

Available on the Unity Asset Store: https://u3d.as/3UC3

### Overview

Simple Circular UI Layout is an easy-to-use component for arranging UI objects along a circle, optionally animating the objects into place as new child objects are added or removed.	

### Setup
	
1.  Attach the component script CircularLayoutGroup to a UI gameobject. Once this component is added, the UI object will function very similarly to VerticalLayoutGroup or HorizontalLayoutGroup, but with the child objects aligned along a circle rather than a straight line. 
2.  Attach child UI objects beneath the main layout object that has the CircularLayoutGroup component. Observe that they are arranged in a circle.
3.  Adjust the size of the parent layout object to control the radius of the alignment circle.
4.  Adjust the settings of CircularLayoutGroup to achieve the desired effect; see below for info on each setting.

### CircularLayoutGroup Settings

* "Circle Size Mode" : The radius of the circle is determined by the size of the layout RectTransform. Change this setting to force the radius to be equal to the Height, Width, or whichever is bigger.
* “Child Alignment" : Determines the center of the circle within the layout RectTransform.
* “Child Pivot" : Determines the point on the child objects that will be used to arrange them around the circle.
* “Child Facing Direction” : By default, child objects will be rotated so that they are facing outward along the circle. Change this setting to InwardAlongNormal to make them face towards the center of the circle instead, or change it to AlwaysUpright to keep the child rotation 0 regardless of its position on the circle.
* “Child Facing Fixed Angle” : If “Child Facing Direction” is set to FixedAngle, this value controls the angle all child objects will be rotated to regardless of their position along the circle.
* “Reverse Arrangement” : By default, child objects will be arranged in ascending child index order. Set this to True to arrange them in descending order instead.
* “Counter-Clockwise” : By default, child objects will be arranged counter-clockwise from “Angle Start”. Set this to False to arrange child object clockwise instead.
* "Angle Start" : The angle at which to start aligning child objects. (Ex. 90 = Straight up)
* "Center Around Start" : If True, the full "Angle Sweep" arc for spreading out child objects will be centered around Angle Start.
* "Angle Sweep" : Maximum arc over which to align child objects, if "Child Force Expand" is set to True.
* "Child Force Expand" : Force all child objects to expand to fill the full "Angle Sweep" arc; otherwise, spacing is determined by "Angle Spacing".
* "Angle Spacing" : Angle between child objects. Does nothing if "Child Force Expand" is set to True.
* "Animate Layout Change" : Should updates to this layout be animated; if false, all changes are instant. Animation will only take place while the game is running. Compatible with DoTween Pro, if you have it installed! 
* "Animate Duration" : The relative (not absolute) amount of time that it takes to animate changes to the layout after child objects are added or removed. If the animation is  happening too quickly, increase this value; if the animation is happening too slowly, decrease this value.

### Technical Notes
* CircularLayoutGroup MUST be attached to an object within a UI canvas! It will not work in 2D or 3D space outside of a canvas.
Compatible with all UI canvas types, all camera types, and all render pipelines.
* CircularLayoutGroup extends the Unity class LayoutGroup, and can be manipulated via code in many of the same ways that Unity layout groups can be manipulated.
* The "Padding" settings under CircularLayoutGroup are an unused remnant of its parent class LayoutGroup and do nothing; adjust the setting "Angle Spacing" with "Child Force Expand" un-checked to achieve a similar spacing control effect. 
* The ContentSizeFitter Unity component is not compatible with CircularLayoutGroup and does nothing.
* Fully compatible with DoTween Pro, and will automatically use its tweening functions if you have it installed; DoTween Pro is NOT required to use Simple Circular UI Layout.


[back](./)
