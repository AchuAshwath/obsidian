08-04-2025 11:57:48

Status : #child

Tags : [[Introduction to JavaScript]] [[DOM]]

# DOM - Document Object Model 

DOM is a built-in object of javascript. which means the example `document.body.innerHTML` is nothing but a object referencing its property, which means that the document is directly linked to the html and the body is a property of the document object and the innerHTML is also a property of the body.

```javascript
> document.title = "javascript"
'javascript'

>document.body.innerHTML = '<button> hello </button>'
'<button> hello </button>'
```

Properties changed on the document aka DOM will reflect in the web page. In addition to properties document object has methods. Which means we can have HTML code inside javascript code, this is the most important feature of the langauage and combines the DOM and HTML together.

```javascript
> console.log(document.title);
Document

> console.log(document.body);
<body> hellow </body>

> console.log(typeof document.body);    // html code inside javascript is a object, so any other object this also has properties and methods eg: innerHTML
 object
```

QuerySelector

```javascript
>console.log(document.body.innerHTML);
<button id = "hellow"> hello </button> <button class = "js-button"> button2 </button>

> console.log(document.querySelector('button'));    // shows the first button
<button id = "hellow"> hello </button>     

> document.querySelector('button')
	 	.innerHTML = 'changed';    // we can put it in a separate line, make sure to indent.
'changed'

> console.log(document.querySelector('button'));
<button> changed </button>

>console.log(document.querySelector('#hellow'));
<button id = "hellow"> hello </button>  

>document.querySelector('.js-button').innerHTML = 'js-button';
'js-button'

```

ClassList - add or remove classes to a selected DOM element.

```javascript
        function subscribe() {
            const subButton = document.querySelector('.js-button');
            // console.log(subButton); // this will give the button tag
            if (subButton.innerText === 'Subscribe') {
                subButton.innerText = 'Subscribed'; // this will change the text of the button when clicked
                subButton.classList.add('js-button-subscribed'); // this will add the class to the button when clicked
            } else {
                subButton.innerText = 'Subscribe'; // this will revert the text of the button when clicked again
                subButton.classList.remove('js-button-subscribed'); // this will remove the class from the button when clicked again
            }
        }
```
## rock-papers-scissors project

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>Rock Paper Scissors</p>
    <button onclick="play('rock');">rock</button>
    <button onclick="play('paper')">paper</button>
    <button onclick="play('scissors')">scissors</button>
    <p class="result"></p>
    <p class="matchup"></p>
    <p id="score-card"></p>
    <button onclick = "
        resetGame();
        showResults();
    ">reset</button>
   <script>
    function pickComputerMove(){
        const randonum = Math.random();
        if(randonum >= 0 && randonum < 0.33) {
            return 'rock';
        } else if (randonum >= 0.33 && randonum < 0.66) {
            return 'paper';
        } else {
            return 'scissors';
        }
    }
    function result(playerChoice, computerMove){
        if(playerChoice === null || computerMove === null) {
            return 'no result';
        }
        else if(playerChoice === computerMove) {
            return 'draw';
        } else if (playerChoice === 'rock' && computerMove === 'scissors') {
            return 'win';
        } else if (playerChoice === 'paper' && computerMove === 'rock') {
            return 'win';
        } else if (playerChoice === 'scissors' && computerMove === 'paper') {
            return 'win';
        } else {
            return 'lose';
        }
    }
    function updateScore(result) {
        if (result === 'win') {
            score.player += 1;
        } else if (result === 'lose') {
            score.computer += 1;
        }
        else if (result === 'draw') {
            score.draw += 1;
        }
        localStorage.setItem('score', JSON.stringify(score));
         
    }
    function resetGame() {
        score.player = 0;
        score.computer = 0;
        score.draw = 0;
        computer_move = null;
        playchoice = null;
        localStorage.removeItem('score');
    }  
    function showResults() {
        document.querySelector('.result').innerHTML = `You ${result(playchoice, computer_move)}!`;
        document.querySelector('.matchup').innerHTML = `You  ${playchoice} - ${computer_move} Computer`;
        document.getElementById('score-card').innerHTML = `Wins : ${score.player} <br> Losses : ${score.computer} <br> Draws : ${score.draw}`
    }
    function play(choice){
        computer_move = pickComputerMove();
        playchoice = choice;
        updateScore(result(playchoice, computer_move));
        showResults();
    }

    let score;
    let computer_move = null;
    let playchoice = null;

    // console.log(localStorage.getItem('score'));
    // if (localStorage.getItem('score')) {
    //     // console.log('score exists in local storage');
    //     score = JSON.parse(localStorage.getItem('score'));
    // }else{
    //     // console.log('score does not exist in local storage');
    //     score = {
    //         player: 0,
    //         computer: 0,
    //         draw: 0
    //     }
    //     // console.log(score);
    // }
    //
    // replacement for the above code
    score = JSON.parse(localStorage.getItem('score')) || {
        player: 0,
        computer: 0,
        draw: 0
    };
   </script> 
</body>
</html>
```
## References

[JavaScript Tutorial Full Course - Beginner to Pro](https://youtu.be/EerdGm-ehJQ?si=YiniT8Ii1jJ32Jn6)

