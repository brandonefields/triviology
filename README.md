
# Triviology
A game about absolutely anything!

## Summary
Triviology is a game of fun & curious facts. We have a wide range of themes spanning sports, science, and arts. Players are presented with trivia questions on cards and multiple choice answers. After an answer is selected, the player is informed of whether their selection is correct and given the option to move on to the next question. Players' points are tracked and they can log back in to continue playing another time.

This game was our first group project while enrolled at Flatiron School. The goal was to not only to exercise our RESTful APIs knowlede and frontend development skills, but also collaborating with other developers and using Git version control.

## Technologies
<img src="https://www.w3.org/html/logo/img/mark-word-icon.png" alt="HTML Logo" height="126">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://upload.wikimedia.org/wikipedia/commons/6/6a/JavaScript-logo.png" alt="Javascript Logo" height="126">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/CSS.3.svg/730px-CSS.3.svg.png" alt="CSS Logo" height="126">

## Setup
Clone(`git clone`) this repo to your local machine. Navigate(`cd <subdirectory name>`) into the newly created directory. 

### Set up your backend
All of the questions/answers data is stored in the `db.json` file. To use this file, if you don't already have a JSON server, in your terminal run `npm install -g json-server`. Then run `json-server --watch db.json`. 

### Set up your front-end
Open another window in your terminal and navigate into the directory where the game files live, aka the newly crated directory after this repository was cloned. Run `lite-server`, the game should open in your browser.

## Features
* Dynamic animations with user interactions
<img src='https://media.giphy.com/media/GgEvaZ7EawNwiivAYX/giphy.gif' height='450'>

* User experience is kept unique by randomizing questions and answers
    (Gif here)

* Players can sign up for an account which keeps track of your progress
    <img src='https://media.giphy.com/media/EfbZw61amWDRpD0nVB/giphy.gif' height='450'>

## Code Snippets
This function is how we pick the next random card. Using recursion, it prevents correctly answered questions from being repeated and handles edge cases:
```javascript
function getRandomNewId(maxId) {
  const randIndex = Math.floor(Math.random() * maxId);
  if (answeredQuestionIds.length === maxId) {
    alert("You've answered all the questions correctly!");
  } else if (answeredQuestionIds.includes(randIndex + 1)) {
    getRandomNewId(maxId);
  } else {
    return randIndex;
  }
  return 0;
}
```

## Future Developments
* User submitted questions
* Skipping undesired questions
* Variable question format
* Variable question difficulty and point values
* User feedback on questions
  

## Reach out
#### Want to get get in touch or see more of our work?
  [Brandon](https://github.com/brandonefields) |
  [Danny](https://github.com/dannyirwin) |
  [Michael](https://github.com/stevemr77)
