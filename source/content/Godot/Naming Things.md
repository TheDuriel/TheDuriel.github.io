## Classes
A Class is written in `PascalCase`, because that's what the engine does.
A Script represents a Class, and should be named the same way for consistency.
A Scene represents a Class, with configuration attached, and can employ the same pattern again for consistency.

`class_name MyAwesomeClass` in `MyAwesomeClass.gd`

## Scene Classes
Additionally we can prefix a Class with a lowercase 'i' to indicate that this class should not be instantiated with .new(), and should only be used to attach it to a Scene.

`class_name iMyAwesomeSceneClass` in `MyAwesomeSceneClass.gd` used by `MyAwesomeScene.tscn`

## Resources

Resource Classes are again using `PascalCase`. But Resources saved to disk prefer `snake_case`. This is so that we can immediately distinguish Classes and Scenes from Resources. Creating two patterns we can follow in the file browser.

`MyAwesomeClass.gd`
`MyResourceClass.gd`
`my_resource_instance.tres`

Spot the odd one out!

## Privacy
GDScript has no concept of Privacy, but we can make do.

Members and Functions using a leading `_` as a prefix will not be shown in the IDE for code completion. They are effectively invisible. If you find yourself typing `Object._function()` You are probably doing something very wrong.

`var _invisible`
`var visible`

## Signals

We prefix Signal callbacks with `_on_<object>_<signal>`

`signal done`
`func _on_done()`
