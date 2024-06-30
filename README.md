# palindrom-checker-project
# Project Description 📝
Create palindrom-checker-project using HTML and CSS,script.js. Apply all the instruction of palindrom-checker-project on freecodecamp.org .

## Demo 📸
life demo : ![Demo](demo.PNG)

here is a demo of palindrom-checker-project .
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
   
    <title>Palindrome Checker</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <main class="container">
 
      <h1 class="title">Sharifa Rezaie palindrome Checker :</h1>
      <div class="palindrome-div">
        <label for="text-input"
          >Enter in text to check for a palindrome:
        </label>
        <input class="palindrome-input" id="text-input" value="" type="text" />
        <button class="palindrome-btn" id="check-btn">Check</button>
        <div class="results-div hidden" id="result"></div>
      </div>
      <div class="palindrome-definition-div">
        <p class="palindrome-definition">
          <span role="img" aria-label="light-bulb">&#128263;</span>
          A <dfn>palindrome</dfn> is a word or sentence that's spelled the same
          way both forward and backward, ignoring punctuation, case, and
          spacing.
        </p>
      </div>
    </main>
    <script src="script.js"></script>
  </body>
</html>
```
```css
body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  background-color: #df3ddc;
  color: #fff;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  width: 100%;
  min-height: 100vh;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.title {
  text-align: center;
  padding: 10px 0;
  font-size: 2.5rem;
  margin-bottom: 20px;
}

.palindrome-div {
  width: 450px;
  min-height: 100px;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  padding: 20px;
  margin: 10px 0;
  background-color: white;
  box-shadow: 0 6px 6px #9ccc2c;
}

.palindrome-definition-div {
  width: 450px;
  font-size: 1.3rem;
  min-height: 140px;
  background-color: #bd5316;
  margin-top: 20px;
  padding: 20px;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

label {
  color: #0a0a23;
  margin-bottom: 20px;
}

.palindrome-input {
  height: 30px;
  width: 250px;
  text-align: center;
  font-size: 1.2rem;
  margin: 10px;
  border: none;
  border-bottom: 2px solid #5a01a7;
}

.palindrome-btn {
  width: 90px;
  border: none;
  padding: 10px;
  border-radius: 15px;
  background-color: #000;
  color: #fff;
  cursor: pointer;
}

.results-div {
  overflow-y: auto;
  word-wrap: break-word;
  min-height: 50px;
  color: black;
}

.user-input {
  font-size: 1.4rem;
  margin-top: 10px;
  text-align: center;
}

.palindrome-definition {
  vertical-align: middle;
  text-align: center;
}

```
```javascript
const userInput = document.getElementById('text-input');
const checkPalindromeBtn = document.getElementById('check-btn');
const resultDiv = document.getElementById('result');

const checkForPalindrome = (input) => {
  const originalInput = input; // Store for later output

  if (input === '') {
    alert('Please input a value');
    return;
  }

  // Remove the previous result
  resultDiv.replaceChildren();

  const lowerCaseStr = input.replace(/[^A-Za-z0-9]/gi, '').toLowerCase();
  const resultMsg = `<strong>${originalInput}</strong> ${
    lowerCaseStr === [...lowerCaseStr].reverse().join('') ? 'is' : 'is not'
  } a palindrome.`;

  const pTag = document.createElement('p');
  pTag.className = 'user-input';
  pTag.innerHTML = resultMsg;
  resultDiv.appendChild(pTag);

  // Show the result.
  resultDiv.classList.remove('hidden');
};

checkPalindromeBtn.addEventListener('click', () => {
  checkForPalindrome(userInput.value);
  userInput.value = '';
});

userInput.addEventListener('keydown', (e) => {
  if (e.key === 'Enter') {
    checkForPalindrome(userInput.value);
    userInput.value = '';
  }
});
```


## Technologies Used 🛠️
List the technologies or tools that i used to develop this project.
script.js
HTML
CSS
## Installation 💻
for using this project you neet to install 3 things:

chrombrowser
an IDE like vscode
git

## Usage 🎯
for using this project you need to know a few commond first clone the repositry in yor local machine then go to the github directory . open the project on your IDE like vscode and start working on it .

go to the cmd and clone the palindrom-checker-project using this commond:

git clone https://github.com/Sharifarezaie/palindrom-checker-project
go to the githu directory:

cd>tribute-page
open the project on your IDE like vscode :

cd>palindrom-checker-project> code .

## Features ⭐
Responsive webpage
-javascript
-github usage


## Author
# sharifaRezaie👩‍💻
LinkedIn: [(https://www.linkedin.com/in/sharifa-rezaie-646636309/)]
Email: [(sharifashaida82@gamil.com)]
## Contributing 🤝
For contribution you can create a pull request and mention me there.Thank you. #

## License