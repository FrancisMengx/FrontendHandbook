## Position
Position is an attribute that manipulate the location of an element. The
value of position attribute work with position-direction
value(left, right, etc.), "nudge" the element into a certain direction.
Depend on the value of the position attribute is, the direction value
works differently.

#### Static
Default value. Element is stick to the normal page flow (take up space).
Directional values(left, right, top, bottom and z-index) has no no effects on the element.

#### Relative
The element’s original position remain in the page flow, just like
static. But left/right/top/bottom/z-index will take effects. However the
positional values(left/right etc.) won’t change the original position in
the flow. Other element’s position won’t be affected by positional value
of the relative elements.  
[Code Demo](https://codepen.io/francismeng/pen/RQMOJd)

#### Absolute
The element is removed from the page flow. Position value is absolute
against the closest position relative/absolute element.
