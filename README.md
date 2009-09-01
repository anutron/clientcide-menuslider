MenuSlider - A simple slide down menu widget
============================================

Slides an element down when the user interacts with a "toggler" element (think drop down menus). So long as the user mouses around inside either the toggler or the menu, it remains visible.

![Screenshot](http://github.com/anutron/clientcide-menuslider/raw/master/screenshot.png)

How to use
----------

### Requires

* [MooTools More 1.2.3.1](http://mootools.net/more): Fx.Slide (and its dependences)
* [HoverGroup](http://github.com/anutron/clientcide-hovergroup/tree/master) (and its dependencies)


### Syntax

	new MenuSlider(menu, subMenu, options);

### Arguments

1. menu - (*mixed*) A string of the id for an Element or an Element reference for the menu item that triggers the slide down of the submenu
2. submenu - (*mixed*) A string of the id for an Element or an Element reference that slides down into view when the user mouses over the menu
3. options - (*object*) An object of key/value settings

### Options

* onIn - (*function*) A callback executed when the menu slides in.
* onOut - (*function*) A callback executed when the menu slides out.
* hoverGroupOptions - (*object*) Values passed to the instance of [HoverGroup][] used by the class.
* fxOptions - (*object*) Values passed to the instance of [Fx.Morph][] used by the class.
* useIframeShim - (*boolean*; defaults to *true*) If *true* and [IframeShim][] is present in your environment, the class integrates with IframeShim to shim the sub-menu.
* outFx - (*boolean*) if *true* the menu slides out when hidden; otherwise hides immediately (the default);

### Example

	var myMenu = new MenuSlider($('menuItem'), $('slideDown'));

MenuSlider method: slideIn {#MenuSlider:slideIn}
------------------------------------------------

Slides the submenu into view.

### Example

	myMenu.slideIn();

### Returns

* *object* - This instance of [MenuSlider][].


MenuSlider method: slideOut {#MenuSlider:slideOut}
-------------------------------------------------

Slides the submenu out of view. Note that, by default, there is no animation for this behavior.

### Syntax

	myMenu.slideOut(useFx);

### Arguments

1. useFx - (*boolean*) if *false* the menu hides immediately (same as calling *.hide*). If not specified, uses the value of *outFx* in the options (defaults to *false*).

### Returns

* *object* - This instance of [MenuSlider][].

MenuSlider method: hide {#MenuSlider:hide}
------------------------------------------

Immediately hides the submenu.

### Example

	myMenu.hide();

### Returns

* *object* - This instance of [MenuSlider][].

MenuSlider method: isVisible {#MenuSlider:isVisible}
------------------------------------------

Returns *true* if the slider is visible (or in the process of displaying).

### Example

	myMenu.isVisible(); //true if visible

### Returns

* *boolean* - *true* if the slider is visible or in the process of displaying.

[IframeShim]: /Browser/IframeShim
[Options]: http://www.mootools.net/docs/core/Class/Class.Extras#Options
[Events]: http://www.mootools.net/docs/core/Class/Class.Extras#Events
[MenuSlider]: /Layout/MenuSlider