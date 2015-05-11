# Rock-Paper-Scissors-Lizard-Spock
A simple game of rock, paper, scissors that I expanded on at codeacademy.com





/* WELCOME TO ROCK, PAPER, SCISSORS, LIZARD, SPOCK VER 1.1 */

/*ask user to make a choice*/
var userChoice = prompt("Welcome to Rock, Paper, Scissors, Lizard, Spock. Do you choose rock, paper, scissors, lizard or spock?");

/*making responses quicker via variables, also announcing the winner.*/
var improper = "Not a valid answer.  Please try again.";
var rock = "rock wins.";
var paper = "paper wins.";
var scissors = "scissors wins.";
var lizard = "lizard wins.";
var spock = "spock wins.";
var victorUser = "You are the winner!"
var victorComputer = "You lost to the superior might of the computer!"

/*computer makes a choice*/
var computerChoice = Math.random();
if (computerChoice < 0.21) {
	computerChoice = "rock";
}else if(computerChoice <= 0.41) {
	computerChoice = "paper";
}else if(computerChoice <= 0.61) {
    computerChoice = "scissors";
}else if(computerChoice <= 0.81) {
    computerChoice = "lizard";
}else {
	computerChoice = "spock";
}

/*log the choices of user and computer in the console*/
console.log("Computer: " + computerChoice);
console.log("You: " + userChoice);

/*make a comparison of choices and return the winner */
var compare = function (choice1, choice2) {
    if (choice1 === choice2) {
        return "The result is a tie!"
    }
    else if (choice1 ==="rock") {
        if (choice2 ==="paper") {
            return paper + " " +victorComputer
        }
        else if (choice2 ==="scissors") {
            return scissors + " " + victorUser
        }
        else if (choice2 === "lizard") {
            return lizard + " " +victorUser
        }
        else if (choice2 === "spock") {
            return spock + " " +victorComputer
        }
        else {
            return improper
        }
    }
    else if (choice1 === "paper") {
        if (choice2 === "rock") {
            return paper + " " +victorUser
        }
        else if (choice2 === "scissors") {
            return scissors + " "+ victorComputer
        }
        else if (choice2 === "lizard") {
            return lizard + " " +victorComputer
        }
        else if (choice2 === "spock") {
            return paper + " " +victorUser
        }
        else {
            return improper
        }
    }
    else if (choice1 === "scissors") {
        if (choice2 === "rock") {
            return rock + " " +victorComputer
        }
        else if (choice2 === "paper") {
            return scissors + " " +victorUser
        }
        else if (choice2 === "lizard") {
            return scissors + " "+ victorUser
        }
        else if (choice2 === "spock") {
            return spock + " " +victorComputer
        }
        else {
            return improper
        }
    }
    else if (choice1 === "lizard") {
        if (choice2 ==="rock") {
            return rock + " " +victorComputer
        }
        else if (choice2 === "paper") {
            return lizard + " " +victorUser
        }
        else if (choice2 === "scissors") {
            return scissors + " "+ victorComputer
        }
        else if (choice2 === "spock") {
            return lizard + " " +victorUser
        }
        else {
            return improper
        }
    }
    else if (choice1 === "spock") {
        if (choice2 === "rock") {
            return spock + " " +victorUser
        }
        else if (choice2 === "paper") {
            return paper + " " +victorComputer
        }
        else if (choice2 === "scissors") {
            return spock + " " +victorUser
        }
        else if (choice2 === "lizard") {
            return lizard + " " +victorComputer
        }
        else {
            return improper
        }
    }      
    else {
        return improper
    }
    
};
    
/* call the functions */
compare(userChoice, computerChoice)
