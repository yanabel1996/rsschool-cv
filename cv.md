# Resume  

![My photo](img/photo.JPG)
  
##  Personal information  

### Name  
Iana Belousova  

### Location  
Plzen, Czech Republic

### Contact information 
Email: <yanabelousova1996@gmail.com>  
LinkedIn profil: <https://www.linkedin.com/in/iana-belousova-753881257/>  
GitHub: yanabel1996  
Telegram: <https://t.me/whitemustache25>  
Discord: Iana_Belousova#6687

###  About
I am a committed and responsible person, I love to develop and learn something new. There are no impossible tasks for me. My goal is to become a successful specialist in Frontend development. At the moment I have no experience in this field, but I have training projects. 

### Skills  
I have good knowledge of HTML, CSS, BEM methodology. I know the basics of JavaScript, Bootstrap, I know how to use various JS libraries, work with documentation, I know the Git version control system. I can do simple animation with JavaScript and libraries. Also, I have a high level of Figma, Photoshop and Tilda.

### Work experience  
- Landing W-Wave Radio(2023) - training project
- Landing Skillbox(2022) - training project
- Landing Lionic(2022) - training project
- Landing Евклид(2022) - training project
- Landing Lagoona(2022) - training project

### Education  
- USMA 2014-2020гг. - therapist
- University of West Bohemia 2021-2024гг. - teacher of Russian as a foreign language
- Skillbox 2020-2023гг. - profession Fullstack designer(HTML, CSS, BEM methodology, JavaScript, Bootstrap)
- Brainnest trainee 2023г. - trainee for Frontend developers

### Languages 
- English - Upper-Intermediate(B2)
- Czech - Intermediate(B1+)
- Russian - Native  

## Example of code  
Game in the console "Stone, scissors, paper"  
 
        function computerPlay() {
            let result;
            let randomNumber = Math.random();
            if (randomNumber <= 0.33) {
                result = `Rock`;
            } else if (randomNumber <= 0.67) {
                result = `Paper`;
            } else {
                result = `Scissors`;
            }
            return result;
        }
        let computerScore = 0;
        let playerScore = 0;

        function game() {
            console.log(`Let's play the game "Rock, Paper, Scissors"!`)
            for (let i = 1; i < 6; i++) {
                console.log(`---ROUND №${i}---`);
                function playRound(playerSelection, computerSelection) {
                    playerSelection = prompt('Put your choice: Rock, Paper or Scissors?');
                    computerSelection = computerPlay();
                    let playerAnswer = playerSelection.toLowerCase();
                    if (computerSelection === playerAnswer) {
                        computerScore++;
                        playerScore++;
                        return console.log("The friendship won!");
                    } else if (playerAnswer === `scissors`) {
                        if (computerSelection === `Rock`) {
                            computerScore++;
                            return console.log("You Lose! Rock beats Scissors!");
                        } else {
                            playerScore++;
                            return console.log("You Win! Scissors beats Paper");
                        }
                    } else if (playerAnswer === `rock`) {
                        if (computerSelection === `Paper`) {
                            computerScore++;
                            return console.log("You Lose! Paper beats Rock");
                        } else {
                            playerScore++;
                            return console.log("You Win! Rock beats Scissors");
                        }
                    } else if (playerAnswer === `paper`) {
                        if (computerSelection === `Scissors`) {
                            computerScore++;
                            return console.log("You Lose! Scissors beats Paper");
                        } else {
                            playerScore++;
                            return console.log("You Win! Paper beats Rock");
                        }  
                    }
                    playerScore;
                    computerScore;
                }
                playRound();
            }
            return console.log(`Game is over! Results: Computer = ${computerScore}, Player = ${playerScore}`);
        }