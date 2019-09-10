# CFML DogAPI
A CFML wrapper for [The Dog API](https://dog.ceo/dog-api/documentation/).  
Interact with the self-proclaimed largest open source collection of dog pictures on the internet.

*Feel free to use the issue tracker to report bugs or suggest improvements!*

### Acknowledgements

This project borrows heavily from the API frameworks built by [jcberquist](https://github.com/jcberquist), such as [xero-cfml](https://github.com/jcberquist/xero-cfml) and [aws-cfml](https://github.com/jcberquist/aws-cfml). Because it draws on those projects, it is also licensed under the terms of the MIT license.

## Table of Contents

- [Quick Start](#quick-start)
- [`CFML DogAPI` Reference Manual](#reference-manual)

## Quick Start
Who needs cats for demos? Looking for a random dog image? Here you go:

```cfc
dogapi = new path.to.cfmldogapi.dogapi();

randomDog = dogapi.getRandomImage().data.message;

writeOutput( '<img src="#randomDog#" />' );
```

## Reference Manual

#### `getRandomImage()`
Display a single random image from all dogs collection

#### `listRandomImages( numeric count = 1 )`
Returns multiple random images from all dogs collection

#### `listBreeds()`
Lists all available breeds (and sub-breeds)

#### `listImagesByBreed( required string breed )`
Lists all the images from a breed, e.g. hound

#### `getRandomImageByBreed( required string breed )`
Returns a random dog image from a breed, e.g. hound

#### `listRandomImagesByBreed( required string breed, numeric count = 1 )`
Returns multiple random dog images from a breed, e.g. hound

#### `listSubBreedsByBreed( required string breed )`
Lists all the sub-breeds from a breed

#### `getRandomImageBySubBreed( required string breed, required string subbreed )`
Returns a single random image from a sub-breed

#### `listRandomImagesBySubBreed( required string breed, required string subbreed, numeric count = 1 )`
Return multiple random dog images from a sub-breed, e.g. Afghan Hound

#### `listImagesBySubBreed( required string breed, required string subbreed )`
Lists all the images from the sub-breed, e.g. Boston Bulldog

---
