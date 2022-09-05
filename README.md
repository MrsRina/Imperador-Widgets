# Imperador-Widgets

What is this? Imperador widgets is a entry box source code, it has copy | paste | delete + words | backward + words | select | scroll | type
How to use it? This was developed into Minecraft context, but you can look the code and use it how you want.

For you implement in your game/client/project, remember, the code use OpenGL, the scissor!
You can replace the all render methods on the code with your own classes!

# Configuration

```java
final ImperadorEntryBox entry = new ImperadorEntryBox(new TurokFont(new Font(...)), "default_text");

entry.scissor(); // For you sync automatically the space.
// Or you can edit the scissor!
entry.getScissor(); // Its a TurokRect class!
// The scissor works for label, button & entry.

// For you set the size of entry/label/button!
entry.getRect();

// The label/button have center, left & right methods;
label.center();
label.left(int offset);
label.right(int offset);
// Or edit.
label.setOffsetX(int v);

// You can modify the string offset Y!
label.setOffsetY(int v);

// The entry box have a Save entry!
final String typing = entry.getText(); // The current typed!
final String last = entry.getSave(); // The last text before unfocus!

```

# Events

```java
final TurokMouse mouse = new TurokMouse(mousePositionX, mousePositionY);

// For entry box, you always need update the scroll!
entry.doMouseScroll(mouse);

// For you sync the mouse over of entry/button;
button.doMouseOver(mouse);

// The event click for button & entry is the mouseClicked(int mx, int my, int button) (Minecraft GUI);
button.onMouseClicked(button);
entry.onMouseClicked(button);
// Remember do onMouseReleased in mouseReleased (Minecraft GUI);
entry.doSetIndexAB(button); // For sync the entry box selections.

// For entry box keytyped, the keyTyped method in (Minecraft GUI);
entry.onKeyboardPressed(char character, int key);

```
