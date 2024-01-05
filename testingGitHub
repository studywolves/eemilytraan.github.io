# emilyytrann.github.io

# Coding Made Easy: Python
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Made with Github")

### Printing
```python
print("Hello World")
print("""
      This will print exactly as it is written in this box.
      """)
print("")
### Will print an indention
```

### Concatentation
```python
print(food, "with", badFood, plant, "on a bed of", item)
### , will print out the users input with a space automatically in between
print(food + " with " + badFood + “ ” + plant + " on a bed of " + item)
### + you have to place in the spaces where you want them
```

### Print in Color
> # “\033[m”

```python
print("You have a", "\033[31m" + "warning" + "\033[0m", "code.")
### You have a warning code. with warming red
print("You have a", "\033[31m", "warning", "\033[0m", "code.")
### You have a  warning  code. with a warning red but with extra spaces
```
| **Color**   | **Value** |
|---------|-------|
| Default | 0     |
| Black   | 30    |
| Red     | 31    |
| Green   | 32    |
| Yellow  | 33    |
| Blue    | 34    |
| Purple  | 35    |
| Cyan    | 36    |
| White   | 37    |

### If-Else Statements
```python
myName = input("What's your name?: ")
if myName == "David":
  print("Hello David!")
  print("You're the baldest person ever.")  
elif myName == "Emily":
  print("Hi Emily!")
else:
  print("You're not David?!")
### will print something for David, something for Emily, and something for everything else
```
| == | =! | <= | >= | <> |
|----|----|----|----|----|
| equal to | not equal to | less than or equal | greather than or equal | less than / greater than |



```javascript
// Create and assign lists of names and their coresponding categories.
// Will be used when filtering the lists below.
var calories    = getColumn("Cereal Nutrition","Calories");
var sugars      = getColumn("Cereal Nutrition", "Grams of Sugars");
var names       = getColumn("Cereal Nutrition", "Name");

// Lists for when I filter. The elements will be filtered into there empty lists.
var filteredNames     = [];
// Lists with details about common nutritional facts.
var filteredCalories  = [];
var filteredSugars    = [];

// Filtering the table.
// These new variables will be added to the end of the filtered Name lists above.
var name;
var calorie;
var sugar;




// Function that filters the lists into empty lists.
function filter(number, nutrition, nutritions, filteredNutritions) {
  // The names will loop until the end of the column "names" of the data Cereal Nutrition.
  for(var i = 0; i < names.length; i++){
    
  // Makes the name and calorie/sugar on the same index number when it is filtering.
    nutrition   = nutritions[i];
    name         = names[i];

    // Uses the variable number to filter through the list.
    // Number is the dropdown on either the calorie or sugar screen.
    // This selection statement will match the user's input to the data in the table.
    if (number == nutrition){
      // Will add each of these categories to the Science lists.
      appendItem(filteredNames, name);
      appendItem(filteredNutritions, nutrition);
    
    // If the number chosen does not match ANY number from the column chosen,
    // the image will tell the user that there is no cereal that matches that data.
    } else {
        setProperty("calorieImage", "text", "There is no cereal that matches that amount. Please choose another number!");
        setProperty("sugarImage", "text", "There is no cereal that matches that amount. Please choose another number!");
    }
  }
}




// Calls the function filterNutrition with parameters.
filterNutrition ("calorieDropdown", "calorieImage", calorie, calories, filteredCalories);
filterNutrition ("sugarDropdown", "sugarImage", sugar, sugars, filteredSugars);


// Filters the lists based on the screen.
function filterNutrition (dropDown, image, nutrition, nutritions, filteredNutritions){
  onEvent(dropDown, "change", function(){
    // Clears the lists when you change the calories.
    // This helps to not combine the calories of different amounts.
    filteredNames     = [];
    filteredCalories  = [];
    filteredSugars    = [];

      // Calls the function filter to traverse the list.
      filter(getText(dropDown), nutrition, nutritions, filteredNutritions);
  
  // This is the automatic image that tells the user how the program works.
  setProperty(image, "background-color", rgb(255,255,255));
  setProperty(image, "text", "Click on the arrows below to see your selection of cereals");
  });
}




// Uses the function updateScreen to change the images for each screen.
updateScreen("calorieLeft", "calorieRight", "calorieImage");
updateScreen("sugarLeft", "sugarRight", "sugarImage");


// Changes the images.
var namesIndex = 0;

// When the left arrow is clicked, the name subtracts 1 from the index, allowing the image to change.
// It only does this as long as an index exists.
function updateScreen(leftArrow, rightArrow, image){
  onEvent(leftArrow, "click", function() {
    
    // As long as the index is greater than 0, then you can go backwards in the list.
    if (namesIndex > 0){
      namesIndex = namesIndex - 1;

    // If the index is 0, that means that something does not inside the list. 
    } else
        namesIndex = filteredNames.length-1;

    updateImage(image);
    });


  // When the right arrow is clicked, the name adds 1 from the index, allowing the image to change.
  // It only does this as long as an index exists, and it loops around.
  onEvent(rightArrow,"click",function(){
    
    // As long as the current index that the picture is on is within the length of the list,
    // You can go forwards in the list.
    if (namesIndex < filteredNames.length - 1){
      namesIndex = namesIndex + 1;

    // If the index is not within the list, then the function does not work.
    } else
        namesIndex = 0;

    updateImage(image);
    });
}


// This function helps change the image.
function updateImage (image){
  // If the filteredNames is filled, the left and right arrows will work.
  if (filteredNames.length == 0){
    setProperty(image, "background-color", rgb(255,255,255));
    setProperty(image, "text", "There is no cereal that matches that amount. Please choose another number!"); 
    
  // If no cereal exists in the chosen calorie amount, an image will tell the user that none exists.
  } else {
      var currentName = filteredNames[namesIndex];
      setProperty(image, "background-color", rgb(randomNumber(0,255),randomNumber(0,255),randomNumber(0,255)));
      setProperty(image, "text", currentName);
  }
}




// Help the user change screens, using the function changeScreen with parameters.
changeScreen("calorieButton", "calorieScreen", "calorieImage");
changeScreen("sugarButton", "sugarScreen", "sugarImage");
homeScreen("homeButton1", "homeScreen");
homeScreen("homeButton2", "homeScreen");


// Uses the parameters to make a cleaner code to take the user to the homeScreen.
function homeScreen (button, screen){
  onEvent(button, "click", function(){
    setScreen(screen);
  }
)}

// Uses the parameters to make a cleaner code to take the user to one of the nutrition screens.
function changeScreen (button, screen, image){
  onEvent(button, "click", function(){
    setScreen(screen);
    // This is the automatic image that tells the user how the program works.
    setProperty(image, "background-color", rgb(255,255,255));
    setProperty(image, "text", "Click on the arrows below to see your selection of cereals");
  }
)}




// Description: cereal nutrition facts of the top selling cereals.
// Source (data): Kaggle
// Processing: renamed some columns for clarity.
// Data table provided by CODE.org.
// All icons provided by the free CODE.org clip art library.

// Images and data provided by CODE.org
// Creative Commons License (CC BY-NC-SA 4.0).
// This work is available under a Creative Commons License (CC BY-NC-SA 4.0).
// https://studio.code.org/data_docs/cereal-nutrition/

// This program was inspired by lessons from CODE.org Unit 4, 5, 6, and 7 circiculumm and Mr.Kaiser's CODE.org walkthroughs.
// It was majorly modifided to fit my ideas and data set.
```
