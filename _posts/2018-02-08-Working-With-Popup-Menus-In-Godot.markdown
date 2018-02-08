---
title: "Working With Popup Menus In Godot"
date: 2018-02-08 11:20:00 -05:00
categories:
- Godot
- Dev
- Programming
tags:
- Godot
- Popup menu
- Programming
- Guide
layout: post
author: Chuck Lindblom
---

# Popup Menus Is Godot
Last night I started work on a test project, and I wanted to start using popup menus correctly. I had implemented them in my game 'LightsOut!' but I did not relize that I was using them incorrectly. As it turns out this Node is super helpful and pretty easy to use if you now what you are doing.

## Working With The Popup Menu Node
{% include image.html url="/img/GodotPopupNodes.png" description="Godot Node Structure" %}
{% highlight python %}
extends Node

# Internal Connections
onready var popup = self.get_node("PopupMenu")

func _ready():
	_setupPopupMenu()

func _setupPopupMenu():
	# This function will clear the popup menu and then add the items to it
	popup.clear()
	popup.add_item("Item1", 1)
	popup.add_item("Item2", 2)
	popup.add_item("Item3", 3)
	popup.set_position(Vector2(100,100))
	popup.connect("id_pressed", self, "_popupMenuChoice")
	popup.show()

func _popupMenuChoice(ID):
	# This function takes the ID of the chocie you made and runs something
	if ID == 1:
		print("You picked Item1")
	elif ID == 2:
		print("You picked Item2")
	elif ID == 3:
		print("You picked Item3")
{% endhighlight %}
