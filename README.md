# jQuery FakeType
FakeType allows you to automatically "type" a string into an attribute of an element.  

## Usage

    $element.fakeType(string, options)

- ```string```: The string that will be automatically written.
- ```options```: An object specifying options.

### Options
- ```timeout```: The number of miliseconds between each consecutive string element.
- ```attribute```: The attribute in which to type.
- ```beforeEach```: A callback that is invoked with the next string element to be written. The return value of the callback will be the next written thing.
- ```done```: A callback that is invoked once the entire string has been written.

## Example

    var placeholder = 'Type something here!';
    
    ...

    $input.fakeType(placeholder, {
      beforeEach: function(char) { return char.toUpperCase(); },
      done: function() { doThisAgain(); },
      attribute: 'placeholder',
      timeout: 200
    });