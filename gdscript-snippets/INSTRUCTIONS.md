# 📖 How to Run & Test Snippets in Godot 3.5.3

This guide explains how to use this snippet library and test pure GDScript logic instantly inside the editor using `EditorScript`, without needing a running game window, cameras, or complex 2D scenes.

---

## 🚀 Part 1: Your First "Hello World" Test

Before copying advanced movement or physics scripts, use this simple boilerplate to verify your setup.

### 1. Create the Script File
Inside your Godot project, create a new script named `hello_world.gd` and paste this exact template:

```gdscript
tool
extends EditorScript

# The _run() function fires automatically when triggered in the editor workspace
func _run():
	print("")
	print("====================================")
	print("SUCCESS! Your script playground is active!")
	print("====================================")
	print("")
```

### 2. How to Execute It
1. Open the script inside your **Godot 3.5.3** interface.
2. Go to the top menu bar, click on **Scene**, and select **Run Script** (or use the fast shortcut **Ctrl + Alt + X**).
3. Look directly at the **Output panel** at the absolute bottom of the Godot editor screen. Your printed statements will instantly show up right there!

---

## 💡 The Core Blueprint Rules

To write or test your own standalone scripts in this environment, always keep these four absolute rules in mind:

1. **`tool`**: This keyword must always sit at the absolute top (line 1). It forces the engine to let the file execute code logic straight inside the workspace editor.
2. **`extends EditorScript`**: This tells Godot that this script is a lightweight utility piece rather than a script meant to be physically attached to a standard game node (like a `KinematicBody2D` or `Sprite`).
3. **`func _run():`**: Godot explicitly searches for the `_run()` function to pass the execution loop the exact moment you hit the manual trigger command. Put all your initial terminal testing code here!
4. **🐍 The Python Rule (It's the Exact Same Logic!)**: If you already know Python, **you already know GDScript!** They both use whitespace indentation instead of curly braces `{}`, statements end automatically without semicolons `;`, and standard control loops (`if`, `for`, `while`) function identically. The logic translates directly—making it incredibly simple to read, write, and trace your scripts like normal sentences.

5.  Attaching to a Node (For Actual Game Snippets): The `EditorScript` method above is just for *testing logic in the editor*. When you're ready to use a snippet in your actual game:
   - Remove `tool` and `extends EditorScript` — replace with whatever node type the snippet needs (e.g. `extends KinematicBody2D`, `extends Sprite`, `extends Node2D`, etc.)
   - In the **Scene panel** (left side), select the node you want the script on.
   - **Right-click** the node → click **"Attach Script"** (or click the 📜 icon that appears at the top of the Scene panel).
   - A dialog pops up → set the path/name for your `.gd` file → click **Create**.
   - You'll now see a small script icon next to the node in the Scene panel, and the script shows up in the **Inspector** (right side) under the `script` property.  That means it's attached. ✅      
