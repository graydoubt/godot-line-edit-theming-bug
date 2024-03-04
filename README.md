## LineEdit Theming Bug Demo Project

This project demonstrates configured icons using themes in Godot Engine 4.2.1.

The toolbar (`toolbar.tscn`) has a `PlayButton` (`Button` node) and a `SearchBox` (`LineEdit` node).
Both have a configured `theme_type_variation` property, which is set to `Toolbar_PlayButton` and `Toolbar_SearchBox`, respectively.

In the `main.tscn` scene, the top left and right toolbar child scenes are configured to use the `theme_outline.tres` and `theme_solid.tres` to customize the icons.

The `Toolbar_PlayButton`'s `base_type` is set to `Button`, and its `icon` property is configured with a `CompressedTexture2D` of the `res://icons/outline/play-circle.svg` and `res://icons/solid/play-circle.svg`.

The `Toolbar_SearchBox`'s `base_type` is set to `LineEdit`, and its `right_icon` property is also configured with a `CompressedTexture2D` of the `res://icons/outline/magnifying-glass-circle.svg` and `res://icons/solid/magnifying-glass-circle.svg`.

For comparison, the bottom two toolbar instances have editable children enabled and the `PlayButton` and `SearchBox` have their `icon` and `right_icon` (respectively) set directly to the `CompressedTexture2D`.

My expectation is that the top-row toolbar's `SearchBox` (`LineEdit`) would also show the magnifying class as configured in the theme.
Unfortunately, that is not the case.