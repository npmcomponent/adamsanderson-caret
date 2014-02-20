*This repository is a mirror of the [component](http://component.io) module [adamsanderson/caret](http://github.com/adamsanderson/caret). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/adamsanderson-caret`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
caret
=====

Listen to and inspect the text caret.

View the [demo](http://adamsanderson.github.com/caret/) for an example of the information you can get.

Installation
------------

    $ component install adamsanderson/caret

API
---

**Caret(element)**: Create a new text caret observer.  If an `element` is defined, then only changes on that element will be reported.

**caret.on('change', fn)**: Listen for changes to the user's text caret.

**caret.parentElement()**: Returns the parent element containing the text caret.

**caret.textBefore()**: Returns the text before the caret within the current element.

**caret.textAfter()**: Returns the text after the caret within the current element.

Example
-------

    var el = document.getElementById('content');
    var caret = new Caret(el);
    
    caret.on('change', function(){
      var text = this.textBefore();
      var match = text.match(/@(\w+)$/);
      if (match) {
        console.log("Editing user name:", match[1]);
      }
    });


License
-------

  MIT

---

Adam Sanderson, http://monkeyandcrow.com