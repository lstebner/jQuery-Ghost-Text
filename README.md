# Ghost Text

Ghost Text is used to present default text inside of an input and then clear it when the user
gives focus. When the user exits (blurs) the input, if they have not entered their own value
the ghost text is then put back in the input.

## Basic Example
````html
<input id="ghost" type="text" value="Sample Ghost Text" />
````

````javascript
$('#ghost').ghostText();
````

And just like that, the value that it is the text field when the plugin is initiated will become
the "ghost text" and when the input gains focus, it will remove the ghost text for the user to
input whatever they need to. If they blur the input and haven't entered anything, the ghost text
will reappear. Of course, if they've entered any sort of value, the users input will be retained.

That's the most basic usage, but if you'd like you can customize the ghostText a bit.

## Options

````
      ghostText: The text you want to use as the ghost text for this input
          default - current value when .ghostText() is called

      ghostClass: The class to add to the input while the ghost text is present
          default - 'ghost-text'

      focus: A custom callback for when the input gains focus
          default - null

      blur: A custom callback for when the input is blurred
          default - null

      change: A custom callback for when the input value changes
          default - null

      clearOnSubmit: A boolean saying whether or not to clear the input when the parent
              form is submitted if it still has the default ghost text in it.
          default - true

      parentForm: The ID of the parent form to attach the submit event too
          default - A search to find the form using $self.closest('form')
````

## Methods:

````
  - init: An initialization function to set default settings and attach events
  - updateSettings: Update the stored settings for the object
  - parentFormSubmit: Called when parent form is submitted (if clearOnSubmit is true)
  - focus: Called on focus
  - blur: Called on blur
  - change: Call on change
````
	
## Credit
2011 - v1.0 - Created by Luke Stebner and available for public use. If you improve it, share it!

