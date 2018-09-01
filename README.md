# Material Design
Material Design Components for Lazarus, painted with BGRABitmap. Licensed as LGPL v3. 2018 by Lainz.

# Now part of BGRAControls
This component is now part of BGRAControls, is a big step to include this component into a bigger package but it can be done without issues.

# MDButton
This control can act as a normal button, toggle, toggle group, checkbox and radiobutton.

## Getting Started
Drop a MDButton from the Material Design component pallete. By default it has no animation and the colors of a basic Material Design button. You can set the properties you need, listed below.

### Properties
* **Animation**: show or not the ripple effect. Default value: false.
* **Checked**: used with any mode, it shows the button "down" state, and aditionally a glyph (radio button glyph or checkbox glyph). Default value: false.
* **Kind**: it allows you to select the behaviour of the control (normal, toggle, toggle group, checkbox, radiobutton and tab).
* **Style**: Normal, Hover, Active and Disabled colors for button and text.

### Kind
You can use this button with other control functionality like checkbox and radiobutton.

#### CheckBox mode
With this mode, you can select (Checked: true), unselect, invert selection and get selected controls in a group. It's better than you group in a regular TPanel all checkbox buttons.

#### RadioButton mode
Whit this mode, you can select (Checked: true) only one button at a time. You can get the selected control with the method GetSelected explained below. It's better than you group in a regular TPanel all radio buttons.

#### Toggle mode
Like CheckBox mode, but no glyph is added.

#### Toggle Group mode
Like RadioButton mode, but no glyph is added.

#### Tab mode
You can use it like a tab button, to choose only one at a time, and has an animation when you select it.

### Methods
These methods works when a set of MDButton are grouped (better on a Panel). Just call the method on any of the controls in the group.
* **SelectAll**: set all controls Checked property to true. Used when "Kind" property is toggle group or checkbox.
* **UnselectAll**: set all controls Checked property to false. Used when "Kind" property is toggle group or checkbox.
* **InvertSelection**: set all controls Checked property to the opposite. Used when "Kind" property is toggle group or checkbox.
* **GetSelected**: returns a TStringList containing the caption and the MDButton (Objects) that has the property Checked set to true.

### Globals
* **Animate only one button at a time**: with this define, you can limit the number of animations being played at the same time in the whole application for all MDButton controls. Enabled by default.
```pascal
{$DEFINE MDBUTTON_ANIMATEONLYONE} 
```
* **CheckBox and RadioButton glyphs**: you can change in the source of MDButton or by code the next global variables. Notice that the font you use must have these glyphs in each target OS. Modern OS should already have them.
```pascal
var
MDBUTTONBALLOTBOX: string = '✗';
MDBUTTONBALLOTBOXWITHCHECK: string = '✓';
MDBUTTONRADIOBUTTON: string = '🔘';
MDBUTTONRADIOBUTTONCIRCLE: string = '◯';
```
