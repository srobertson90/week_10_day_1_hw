#JS Day 1 Homework

Go through each sample code and work out what the output will be and explain what happened.

### Episode 1
```
var name = 'Keith';

var printName = function() {
  console.log('My name is ' + name );
}

printName();

Output = "My name is Keith"

The portion of code takes in the value of the name variable and injects it into an output string.

```

### Episode 2
```
score = 5;

var result = function() {
  var score = 3;
  return score;
}

console.log(result());

Output = 3

This portion of the code overrides the score variable whithin the function

```

### Episode 3
```
var myAnimals = ['Chickens', 'Cats', 'Rabbits'];

var listAnimals = function() {
  myAnimals = ['Ducks', 'Dogs', 'Lions'];
  for(var i=0;i<myAnimals.length; i++){
    console.log(i + ": " + myAnimals[i]);
  }
}

listAnimals();
Output: 
0: Chickens
1: Cats
2: Rabbits

outputs each array by their index, isn't overwritten in function(?)

```

### Episode 4

```
var suspectOne = 'Jay';
var suspectTwo = 'Val';
var suspectThree = 'Keith';
var suspectFour = 'Rick';

var allSuspects = function() {
  var suspectThree = 'Harvey'
  console.log('Suspects include: ' + suspectOne + ', ' + suspectTwo + ', ' + suspectThree + ', ' + suspectFour)
}

allSuspects();
console.log( 'Suspect three is:' + suspectThree )

Output = "Suspects include: Jay, Val, Harvey, Rick"
"Suspect three is Keith"
suspectThree is overwritten in the first statement but not the second
```

### Episode 5

```
var detective = {
    name : 'Ace Ventura',
    pet : 'monkey'
  }

var printName = function(detective) {
  return detective.name
}

var detectiveInfo = function() {
  detective['name'] = 'Poirot'
  return printName(detective);
}

console.log(detectiveInfo());

Output = "Poirot"
name is overwritten in the function

```

### Episode 6
```
var murderer = 'rick';

var outerFunction = function(){
  var murderer = 'marc';

  var innerFunction = function(){
    murderer = 'valerie';
  }

  innerFunction();
}

outerFunction();
console.log('the murderer is ', murderer);

Output = "The murderer is rick"
the murderer variable isn't overwritten at the point it is outputted
```

### Episode 7 - Make up your own episode/s!

Make up your own episode which can be whatever you wish and the rest of the class will work out together what happened and what the output will be.