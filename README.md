 Tuesday 5th, April
# *Interpreted Language*
## Runs the a program line by line and execute each command, this programming language is cross-platform which makes it faster or easier to test and debug, the source code is public because you need to send to everyone that wants to run the program.

# *Compiled Language*
## Compiled language are converted directly into machine code that the processor can execute, once it's compiled is ready to run, is often faster since it might be optimized for an specific OS or CPU, the source code is private and is not multi-platform and it needs a compiler to debug the program.

# *Is Java compiled or interpreted, or both?* 
## Is a hybrid programming language


# *Pseudocode currency converter*
# You have been selected to develop the algorithm that will be used to convert dollars (USD) to bitcoin (BTC), for this the first thing you must do is deliver a pseudocode with the algorithm to be developed, in this way you can explain in a better way to the team what will be the required operation. The main idea is to have a website where the user will be asked to enter the amount to convert.

1. START
2. BTC <-- 0.000022
3. USD <-- 0.00
4. CONVER <-- 0.00
5. PRINT "Ingrese la cantidad de dolares que quiere convertir a Bitcoins" 
6. USD <-- GET
7. CONVER <-- USD * BTC
8. PRINT "La conversion es: " 
9. PRINT CONVER
10. END

------------------------------------------------------------------------------------------------------------------
Wednesday 6th, April
# *Your date of birth in the matrix?*
## Your team has just seen the movie "Matrix" and you have been asked, how the number of your year of birth would be written in binary. You must learn how to translate your date of birth into binary and show your team. (Do not use a webpage or a tool to convert your date of birth) 

`
11111001001 = 1993 my birthday year
`

# *MIPS*
## Based on the guide and the examples of the low-level language, create the following
- Create a program that adds any two given numbers provided by the user
- Create a program that displays your name 

```
//SOLUTION TO -> Create a program that adds any two given numbers provided by the user
.data
        welcome: .asciiz "\n================= Welcome =================\n"
        result: .asciiz "\nThe result is: "
        number_one_msg: .asciiz "\nEnter the first number: "
        number_two_msg: .asciiz "\nEnter the second number: "
  .text
        main:
              # welcome message
              li $v0, 4
              la $a0, welcome
              syscall

              # user input
              li $v0, 4
              la $a0, number_one_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t0, $v0

              # user input
              li $v0, 4
              la $a0, number_two_msg
              syscall

              li $v0, 5
              syscall

              # saving user input
              move $t1, $v0

              # adding the user numbers
              add $t2, $t0, $t1

              # showing result number
              li $v0, 4
              la $a0, result
              syscall

              # printing number
              li $v0, 1
              move $a0, $t2
              syscall
```

```
//SOLUTION TO -> Create a program that displays your name 
 .data
	      my_name: .asciiz "\nAngello\n"
  .text
	      main:
              li $v0, 4
              la $a0, my_name
              syscall

```

---------------------------------------------------------------------------------------------------------------------
Thrusday 7th, April

# *Exercise 1 / Print special numbers*
## In this exercise you must use an iterative flow control to be able to print all the even numbers in the range of numbers from 0 to 100. Remember that you should not print each number, you should use a flow control structure to perform the exercise

```js
//SOLUTION
console.log('Numbers from 0 to 100 using FOR loop');

var num = 0;

for (var i = 0; i <= 100; i += 2) {
  num = num + i;
  
  console.log(num);
  num = 0;
}
```

# *Exercise 2 / Bad code I*
## The code shown below is not working in the right way, as a task you must find the error made by the developer who programmed this code and correct it, for this exercise you must explain what the error is and place the correct code

```js
//SOLUTION
var cond = true;

if ((cond == true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}
```

# *Exercise 3 / Bad code II*
## You must create the code that follows the following logic, if the given number is 100, take this number as special and show the following message: "This is a special number!", but if the number is less than 1000, multiple of 10 and different from 100, you must show the following message: "This number is almost special". if none of the given conditions are met show the following message: "Just a regular number". Another developer was trying to program the logic, but apparently couldn't, you need to fix the code to work properly

```js
//SOLUTION
var n = 85;

if (n === 100) {
  console.log('This is a special number!');
}
else if (n < 1000 && n % 10 === 0) {
  console.log('This number is almost special');
  console.log('This number is multiple of 10');
} else {
  console.log('Just a regular number');
}
```
-------------------------------------------------------------------------------------------------------------------
Tuesday 19th, April

# *Kata Exercise #1*
## This code does not execute properly. Try to figure out why.

```js
// SOLUTION
function multiply(a, b){
  return a * b
}
```

# *Kata Exercise #2*
## You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters.

examples:

uniTotal("a") == 97 uniTotal("aaa") == 291

```js
// SOLUTION
function uniTotal (myString) {
// total up dem unicodes!
  let total = 0;
  let nLetters = myString.length;
  for (let i = 0; i < nLetters; i++){
    total = total + myString[i].charCodeAt();
  }
  return total;
}
```
# *Kata Exercise #3*
## Write a function get_char() / getChar() which takes a number and returns the corresponding ASCII char for that value.

Example:

get_char(65)

should return:

'A'

```js
// SOLUTION
function getChar(aNumber){
  let vASCII = String.fromCharCode(aNumber);
  return vASCII;
}
```

# *Kata Exercise #4*
## Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.

The binary number returned should be a string.

Example:(Input1, Input2 --> Output (explanation)))

1, 1 --> "10" (1 + 1 = 2 in decimal or 10 in binary)

```js
// SOLUTION
function addBinary(a,b) {
  let sum = a + b;
  let bNumber = new String(sum);
  
  return parseInt(bNumber).toString(2);
}
```

# *Kata Exercise #5*
## Create a function finalGrade, which calculates the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects.

This function should take two arguments: exam - grade for exam (from 0 to 100); projects - number of completed projects (from 0 and above);

This function should return a number (final grade). There are four types of final grades:

- 100, if a grade for the exam is more than 90 or if a number of completed projects more than 10.
- 90, if a grade for the exam is more than 75 and if a number of completed projects is minimum 5.
- 75, if a grade for the exam is more than 50 and if a number of completed projects is minimum 2.
- 0, in other cases

```js
// SOLUTION
function finalGrade (exam, projects) {
 if(exam > 90 || projects > 10){
   return 100
 }
   else if (exam > 75 && projects >= 5){
     return 90
  }
  else if (exam > 50 && projects >= 2){
    return 75
  }
   return 0
}
```
---------------------------------------------------------------------------------------------------------------------------
Wednesday 20th, April

# *Kata Exercise #1*
## The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday.

You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday.

For example, if a bottle cost £10 normally and the discount in duty free was 10%, you would save £1 per bottle. If your holiday cost £500, the answer you should return would be 500.

All inputs will be integers. Please return an integer. Round down.

```js
//SOLUTION

function dutyFree(normalPrice, discount, holidayCost){
  // - Quiero saber cuantas botellas tengo que comprar con el dinero que tengo disponible para mi holiday sin pasarme
  // de mi presupuesto
  // - Quiero saber cuanto vale la botella al precio del descuento
  
  let priceBottle = (normalPrice * discount) / 100;
  // Una vez tengo el precio de la botella tengo que saber cuantas puedo comprar sin pasarme de mi presupuesto
  let howManyB = Math.floor(holidayCost / priceBottle);
  // retornar cuantas ocupo 
  return howManyB;
}
```

# *Kata Exercise #2*
## Your function takes two arguments:

current father's age (years)
current age of his son (years)
Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old).

```js
//SOLUTION

function twiceAsOld(dadYearsOld, sonYearsOld) {
  // your code here
  return Math.abs(dadYearsOld - sonYearsOld - sonYearsOld);
}
```

# *Kata Exercise #3*
## Your task is to write a function called valid_spacing() or validSpacing() which checks if a string has valid spacing. The function should return either true or false (or the corresponding value in each language).

For this kata, the definition of valid spacing is one space between words, and no leading or trailing spaces. Words can be any consecutive sequence of non space characters. Below are some examples of what the function should return:

* 'Hello world'   => true
* ' Hello world'  => false
* 'Hello world  ' => false
* 'Hello  world'  => false
* 'Hello'         => true

Even though there are no spaces, it is still valid because none are needed:
* 'Helloworld'    => true
* 'Helloworld '   => false
* ' '             => false
* ''              => true
Note - there will be no punctuation or digits in the input string, only letters.

```js
//SOLUTION

function validSpacing(string2A) {
  // Necesito saber primero cuantas letras tiene la cadena
  let sizeS = string2A.length; // Esta variable me guarda la cantidad de letras que tiene el string
  // Necesito validar si tengo espacios al principio o al final de la cadena
  if (string2A.charAt(0) === ' ' || string2A.charAt(sizeS - 1) === ' ') {
    // En esta parte valido si inicio del string tengo un espacio o si al final tambien.
    return false;
  }
  else {  
    // Aqui verifico que no tengo doble espacios
    for (let i = 0; i < sizeS; i++) {
      //console.log(string2A.charAt(i)); esta linea la hize para verificar si estaba recorriendo la palabra 
      if (string2A.charAt(i) === ' ' && string2A.charAt(i+1) === ' '){
      return false;
      }
    }
    return true;
    }
  } 
  ```
  
# *Kata Exercise #4*
## Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

Note: input will never be an empty string

```js
//SOLUTION
function fakeBin(stringN){
  if (stringN === ''){
  return false;
  }
  else {
  let newString = '';
  for (let i = 0; i < stringN.length; i++){
    if (stringN[i] < 5){
    newString = newString + '0';
    }
    else {
    newString = newString + '1';
    }
   }
  return newString 
 }
}
```
--------------------------------------------------------------------------------------------------------
Thursday 21st, April

# *Kata Exercise #1*
## Remove all exclamation marks from the end of sentence.


Examples \n
1. remove("Hi!") === "Hi" 
2. remove("Hi!!!") === "Hi" 
3. remove("!Hi") === "!Hi" 
4. remove("!Hi!") === "!Hi" 
5. remove("Hi! Hi!") === "Hi! Hi" 
6. remove("Hi") === "Hi" 

```js
//SOLUTION
function remove(string) {  
let newString = '';
let final = string.length -1;
  
  for (let i = final; i > 0; i--) {
    if (string[i] !== '!'){ 
      newString = string.substring(0, final + 1);
      break;
    }
    else {
      final = final - 1;
      newString = string.substring(0, final + 1);
    }
    
  }
  return newString;
}
```

# *Kata Exercise #2*
## Create a function called shortcut to remove the lowercase vowels (a, e, i, o, u ) in a given string.

Examples
- "hello"     -->  "hll"
- "codewars"  -->  "cdwrs"
- "goodbye"   -->  "gdby"
- "HELLO"     -->  "HELLO"

```js
//SOLUTION
function shortcut (string) {
  let vowels = ['a','e','i','o','u'];
  let newString = '';
  Loop1:
  for (let i = 0; i < string.length; i++) {
    Loop2:
    for (let j = 0; j < vowels.length; j++){
      if (string.charAt(i) === vowels[j]) {
        //continue Loop2;
        continue Loop1;
      }
    }
    newString = newString + string[i];
  }
  return newString;
}
```

# *Kata Exercise #3*
## Rock Paper Scissors
Let's play! You have to return which player won! In case of a draw return Draw!.

Examples:

- rps('scissors','paper') // Player 1 won!
- rps('scissors','rock') // Player 2 won!
- rps('paper','paper') // Draw!

```js
//SOLUTION
const rps = (p1, p2) => {
  if (p1 === p2) { 
    return 'Draw!';
  }
  if (p1 === 'rock' && p2 === 'scissors'){
    return 'Player 1 won!';   
    }
  if (p1 === 'scissors' && p2 === 'paper'){
    return 'Player 1 won!';
  }
  if (p1 === 'paper' && p2 === 'rock'){
    return 'Player 1 won!';
  }
  else
    {
      return 'Player 2 won!';
    }
};
```

# *Kata Exercise #4*
## Persistent Burger
Write a function, persistence, that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.

For example (Input --> Output):

- 39 --> 3 (because 3*9 = 27, 2*7 = 14, 1*4 = 4 and 4 has only one digit)
- 999 --> 4 (because 9*9*9 = 729, 7*2*9 = 126, 1*2*6 = 12, and finally 1*2 = 2)
- 4 --> 0 (because 4 is already a one-digit number)

```js
//SOLUTION
function multiply(times, values) {
  //Callback funtion con paramentros times y values adquiriendo su valores por medio de la funcion persistence
  if(values.length > 1) {
    let newValues = values.reduce((total, n) => total * parseInt(n),1) // aqui creo un nuevo array newValues
      .toString() //Aqui convierto el array newValues a un string
      .split('') //Aqui separo el array por numeros 
    return multiply(times + 1, newValues); //Retorno mi callback funtion si no tengo un numero con mas de un numero
  }
  return times;
}

function persistence(n) {
  return multiply(0, n.toString().split(''));
}
```
----------------------------------------------------------------------------------------------------------
Monday 25th, April

# *Kata Exercise #1*
## Who likes it?
You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement the function which takes an array containing the names of people that like an item. It must return the display text as shown in the examples:

- []                                -->  "no one likes this"
- ["Peter"]                         -->  "Peter likes this"
- ["Jacob", "Alex"]                 -->  "Jacob and Alex like this"
- ["Max", "John", "Mark"]           -->  "Max, John and Mark like this"
- ["Alex", "Jacob", "Mark", "Max"]  -->  "Alex, Jacob and 2 others like this"
Note: For 4 or more names, the number in "and 2 others" simply increases.

```js
//SOLUTION
function likes(names) {
  // recibir los nombres, contar los nombres
  // asignar que mensaje mostrar upon the amount of names
  if(names.length === 0) {
    return `no one likes this`;
  } 
  if(names.length === 1) {
    return `${names[0]} likes this`;
  }
  if(names.length === 2){
    return `${names[0]} and ${names[1]} like this`;
  }
  if(names.length === 3){
    return `${names[0]}, ${names[1]} and ${names[2]} like this`;
  }
  return `${names[0]}, ${names[1]} and ${names.length-2} others like this`;
}
```

# *Kata Exercise #2*
## Bit Counting
Write a function that takes an integer as input, and returns the number of bits that are equal to one in the binary representation of that number. You can guarantee that input is non-negative.

Example: The binary representation of 1234 is 10011010010, so the function should return 5 in this case

```js
//SOLUTION
function countBits(n) {
  // 1. Convertir a binario el numero que recibimos
  // 2. Contar los 1 dentro del arreglo con los numeros binarios
  let nBinary = n.toString(2).split('');
  //console.log('Aqui esta convertido a numero binario ->' + nBinary);
  
  let bitsCount = nBinary.reduce((a,b) => a + parseInt(b), 0);
  // Aqui tomo el arreglo con los numeros binarios y le aplico el metodo reduce para que sume entre si los numeros
  
  return bitsCount;
}
```
# *Kata Exercise #3*
## Your order, please
Your task is to sort a given string. Each word in the string will contain a single number. This number is the position the word should have in the result.

Note: Numbers can be from 1 to 9. So 1 will be the first word (not 0).

If the input string is empty, return an empty string. The words in the input String will only contain valid consecutive numbers.

```js
//SOLUTION
// 1. Convertir el string a un arreglo
// 2. leer cada una de las palabras y encontrar el numero asignado a cada palabra para reordenar el arreglo
// 3. Basado en el numero de las palabras crear un nuevo string con el orden correcto
  

function getWordIndex(word){
  //Aqui creo un High order function para leer cada palabra y reemplazar todos los caracteres que no son
  //numeros con nada ('') para que me devuelva solo el numero que la palabra tiene
  for (let i = 0; i < word.length; i++){
    if (Number(word[i].replace(/\D/g, ''))) return word[i];
  }
}

function order(words){
  // Aqui convierto el string a un arreglo, despues creo un nuevo array que me devolvera el orden correcto
  // Orden de las palabras con el metodo sort y la funcion que cree anteriormente, finalmente convierto el array a un string con join
  let array = words.split(' ');

  let arraySorted = array.sort((firstWord,secondWord) => 
  getWordIndex(firstWord) - getWordIndex(secondWord)); 

  return arraySorted.join(' ');
}
```
----------------------------------------------------------------------------------------------------------
Tuesday 26th, April

# *Kata Exercise #1*
## Simple Pig Latin
Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.

Examples
- pigIt('Pig latin is cool'); // igPay atinlay siay oolcay
- pigIt('Hello world !');     // elloHay orldway !

Note: Numbers can be from 1 to 9. So 1 will be the first word (not 0).

```js
//SOLUTION
// 1. Leer cada una de las palabras, mover cada la primera letra de cada palabra al final de la misma
// 2. Agregar 'ay' al final de cada palabra sin eliminar cualquier signo de puntuacion

function word(str) {
  // En esta funcion reviso cada palabra
    let firstLetter = str.match(/^\w/); // Leo la primera letra y la guardo en firstLetter
    let replacing = str.replace(/^\w/, ''); //Reemplazo la primera letra con nada ('') 
    replacing = replacing.replace(/$/, firstLetter + 'ay'); // agrego la ultima letra al final de la palabra con 'ay'
    return replacing;
}

function pigIt(str){
  let array = str.split(' ');
  let pMarks = ['!', '¡', '?', '¿', '.', ',', ':', ';'];
  let finalString = '';

  for (let i = 0; i < array.length; i++){
      if (pMarks.indexOf(array[i]) >= 0) continue; //Valido que no tengo ningun punctuation mark si lo tengo me lo salto
      array[i] = word(array[i]);  // hago un nuevo arreglo reemplazando las palabras con las que me genera mi funcion word
  }
      finalString = array.join(' ');
      return finalString;
}
```

# *Kata Exercise #2*
## Counting Duplicates
Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.

Example
- "abcde" -> 0 # no characters repeats more than once
- "aabbcde" -> 2 # 'a' and 'b'
- "aabBcde" -> 2 # 'a' occurs twice and 'b' twice (`b` and `B`)
- "indivisibility" -> 1 # 'i' occurs six times
- "Indivisibilities" -> 2 # 'i' occurs seven times and 's' occurs twice
- "aA11" -> 2 # 'a' and '1'
- "ABBA" -> 2 # 'A' and 'B' each occur twice

```js
function duplicateCount(text){
    // 1. to lowerCase
    // 2. split 
    // 3. sort()
    // 4. filter() SOLO METER EL ELEMENT SI ESTA REPETIDO
    //------------------con set
    // 5. set(filter)
    // 6. set to array
    //------------------sin set */
    // 5. Return length del arreglo

    text = text.toLowerCase();
    let duplicatedArray = text.split('').sort();
    //console.log(duplicatedArray);
    let filterArray = duplicatedArray.filter((chr,i) => {
        return duplicatedArray.indexOf(chr, i+1) != -1;
    });
    //console.log(filterArray);
    //let filteredSet = new Set (filterArray);
    //return filteredSet.size;
    // SOLUCION CON EL SET

    let reducer = filterArray.reduce((prev, curr) => {
        if (prev.indexOf(curr) === -1) prev.push(curr);
        return prev;
    },[]);
    return reducer.length;
}
```
# *Kata Exercise #3*
## Decode the Morse code
In this kata you have to write a simple Morse code decoder. While the Morse code is now mostly superseded by voice and digital data communication channels, it still has its use in some applications around the world.
The Morse code encodes every character as a sequence of "dots" and "dashes". For example, the letter A is coded as ·−, letter Q is coded as −−·−, and digit 1 is coded as ·−−−−. The Morse code is case-insensitive, traditionally capital letters are used. When the message is written in Morse code, a single space is used to separate the character codes and 3 spaces are used to separate words. For example, the message HEY JUDE in Morse code is ···· · −·−−   ·−−− ··− −·· ·.

- NOTE: Extra spaces before or after the code have no meaning and should be ignored.

In addition to letters, digits and some punctuation, there are some special service codes, the most notorious of those is the international distress signal SOS (that was first issued by Titanic), that is coded as ···−−−···. These special codes are treated as single special characters, and usually are transmitted as separate words.

Your task is to implement a function that would take the morse code as input and return a decoded human-readable string.

For example:

`decodeMorse('.... . -.--   .--- ..- -.. .')
//should return "HEY JUDE"`
- NOTE: For coding purposes you have to use ASCII characters . and -, not Unicode characters.

The Morse code table is preloaded for you as a dictionary, feel free to use it:

Coffeescript/C++/Go/JavaScript/Julia/PHP/Python/Ruby/TypeScript: 
`MORSE_CODE['.--']`

All the test strings would contain valid Morse code, so you may skip checking for errors and exceptions. In C#, tests will fail if the solution code throws an exception, please keep that in mind. This is mostly because otherwise the engine would simply ignore the tests, resulting in a "valid" solution.

Good luck!

```js
// Funcion secundaria
function decodeEachWord (words){
    let newArray = words.split(' ');
    //console.log(newArray); Aqui primero separo en letras cualquier palabra que le mande
    let newWord = newArray.map((eachLetter) => {
      //let conLetra = eachLetter; Aqui hago un Map para devolver el valor en MORSE_CODE de cada letra que le paso
      return MORSE_CODE[eachLetter];
      });
      return newWord.join(''); 
  }

//Funcion principal
decodeMorse = function(morseCode){
  if (morseCode === '...---...') return MORSE_CODE['...---...']; // Retorno SOS de una sola si me mandan esa palabra
  
  let words = morseCode.split('   ');
  //console.log(typeof words[0]); Aqui separo el statement en palabras
  let newString = [];

  for (let i = 0; i < words.length; i++) {
    newString.push(decodeEachWord(words[i])) //Hago un ciclo for para pasarle cada palabra a la funcion que cree para traducir palabras
  }

  return newString.join(' ').trim(); //Uno cada letra y le paso paso la funcion trim para remover espacios al inicio y final del string final
}
```
----------------------------------------------------------------------------------------------------------
Wednesday 27th, April

# *Kata Exercise #1*
## Valid Parentheses
Write a function that takes a string of parentheses, and determines if the order of the parentheses is valid. The function should return true if the string is valid, and false if it's invalid.

Examples
```
"()"              =>  true
")(()))"          =>  false
"("               =>  false
"(())((()())())"  =>  true
```
Constraints
` 0 <= input.length <= 100 `

```js
//SOLUTION
function validParentheses(parens) {
let parenCount = 0;
  for (let i = 0; i < parens.length; i++) {
    if (parens[i] === ')') {
      parenCount--;
    }
    if (parens[i] === '(') {
      parenCount++;
    }
    if (parenCount < 0) return false;
  }
  return parenCount == 0;
}
```
----------------------------------------------------------------------------------------------------------
Thursday 28th, April

# *Core Challenge - Mission Statement*
## Let’s write our Mission Statement! In one paragraph, please answer to the next 5 questions:

1. Who are you?
2. What background do you have?
3. Who do you want to be?
4. What do you want to do?
5. What are the core values and principles that govern your character and contributions?

```
My name is Angello, I'm a Customer Success Representative with 7+ years of experience,
I'm currently looking to make a change in my career, I'm currently studying programming 
in Javascript, so I can start programming websites so I can have the opportunity to work 
as a Front-end developer or Back-end Developer. I'm always looking to improve in life, 
I have taught myself to be persistent and do the best I can so I can resolve any issues
I face in life. My main goal in life is to become a better version of myself.
```

---------------------------------------------------------------------------------------------------------
Wednesday 4th, May

# *Kata Exercise #1*
## Simple validation of a username with regex
Write a simple regex to validate a username. Allowed characters are:

- lowercase letters,
- numbers,
- underscore
Note: Length should be between 4 and 16 characters (both included).

```js
// SOLUTION
function validateUsr(username) {
 /**
    - `^`        Start from the beginning of the string.
    - `[]`       Allow any character specified, including...
    - `0-9`      anything from 0 to 9,
    - `a-z`      anything from a to z,
    - `_`        and underscore.
    - `{4,16}`   Accept 4 to 16 of allowed characters, both numbers included.
    - `$`        End the string right after specified amount of allowed characters is given.
  */
  let res =  /^[0-9a-z_]{4,16}$/   
  return res.test(username)
}
```
# *Kata Exercise #2*
## Get number from string
Write a function which removes from string all non-digit characters and parse the remaining to number. E.g: "hell5o wor6ld" -> 56

Function: `getNumberFromString(s)`

```js
// SOLUTION
function getNumberFromString(s) {
  let regex = /\D/g
  let numero = parseInt(s.replace(regex, ''));
  return numero;
}
```

---------------------------------------------------------------------------------------------------------
Thursday 5th, May

# *Kata Exercise #1*
## String cleaning
Your boss decided to save money by purchasing some cut-rate optical character recognition software for scanning in the text of old novels to your database. At first it seems to capture words okay, but you quickly notice that it throws in a lot of numbers at random places in the text.

Examples (input -> output)
```
'! !'                 -> '! !'
'123456789'           -> ''
'This looks5 grea8t!' -> 'This looks great!'
```

Your harried co-workers are looking to you for a solution to take this garbled text and remove all of the numbers. Your program will take in a string and clean out all numeric characters, and return a string with spacing and special characters ~#$%^&!@*():;"'.,? all intact.

```js
//SOLUTION
function stringClean(s){
    let reg = /\d/g  /*Aqui lo que hago esque encuentro cualquier caracter que sea un numero para despues reemplazarlo   
    por nada '' con la funcion .replace()*/
    let newString = s.replace(reg, '');
    return newString;
  }
```

# *Kata Exercise #2*
## Regex Password Validation
You need to write regex that will validate a password to make sure it meets the following criteria:

- At least six characters long
- contains a lowercase letter
- contains an uppercase letter
- contains a number
- Valid passwords will only be alphanumeric characters.

```js
//SOLUTION 1
function validate(password) {
// ^               # start of input 
// (?=.*?[A-Z])    # Lookahead to make sure there is at least one upper case letter
// (?=.*?[a-z])    # Lookahead to make sure there is at least one lower case letter
// (?=.*?[0-9])    # Lookahead to make sure there is at least one number
// [A-Za-z0-9]{6,} # Make sure there are at least 6 characters of [A-Za-z0-9]
// $               # end of input
  return /^(?=.*?[A-Z])(?=.*?[a-z])(?=.*?[0-9])[A-Za-z0-9]{6,}$/.test(password);
}
``` 

```js
//SOLUTION 2
function validate(password) {
  // least six characters long --> {6,}
  // contains a lowercase letter --> [a-z]+
  // contains an uppercase letter --> [A-Z]+
  // contains a number --> [0-9]+
  
  return (/^[a-zA-Z0-9]{6,}$/.test(password) 
        && /[a-z]+/.test(password)
        && /[A-Z]+/.test(password)
        && /[0-9]+/.test(password)
         );
}
```
---------------------------------------------------------------------------------------------------------
Monday 9th, May

# *Kata Exercise #1*
## Find the missing letter
Write a method that takes an array of consecutive (increasing) letters as input and that returns the missing letter in the array.

You will always get an valid array. And it will be always exactly one letter be missing. The length of the array will always be at least 2.
The array will always contain letters in only one case.

Example:
```
['a','b','c','d','f'] -> 'e' ['O','Q','R','S'] -> 'P'

["a","b","c","d","f"] -> "e"
["O","Q","R","S"] -> "P"
```
(Use the English alphabet with 26 letters!)

```js
//SOLUTION
function findMissingLetter(array){
  let newArray = array.map((char) => char.charCodeAt());
  // Aqui convierto el arreglo de letras en el codigo equivalente de cada letra en la tabla ASCII
  //console.log(newArray);  Prueba
  let missingFoundCode = '';
  
  for (let i = 1; i < newArray.length; i++) {
    //console.log('Esto vale i -> ' + newArray[i] + ' Esto vale i + 1 -> ' + newArray[i-1]); Prueba
    if (newArray[i] - newArray[i - 1] == 2) {
      //Aqui recorro el array empezando desde la posicion 1 y lo resto con la posicion 
      //anterior para saber el valor de diferencia entre los valores, dos numeros de  
      //diferencia activan mi statement true y con eso puedo encontrar el codigo que busco si le resto uno
      //console.log(newArray[i]); Prueba
      missingFoundCode = newArray[i] - 1; // 
      //console.log(missingFoundCode) Prueba
    }
  }

  return String.fromCharCode(missingFoundCode); // Una vez encontrado el codigo busco su valor en la ASCII table
}
``` 
# *Kata Exercise #2*
## Reverse or rotate?
The input is a string str of digits. Cut the string into chunks (a chunk here is a substring of the initial string) of size sz (ignore the last chunk if its size is less than sz).

If a chunk represents an integer such as the sum of the cubes of its digits is divisible by 2, reverse that chunk; otherwise rotate it to the left by one position. Put together these modified chunks and return the result as a string.

If
- sz is <= 0 or if str is empty return ""
- sz is greater (>) than the length of str it is impossible to take a chunk of size sz hence return "".

```
Examples:
revrot("123456987654", 6) --> "234561876549"
revrot("123456987653", 6) --> "234561356789"
revrot("66443875", 4) --> "44668753"
revrot("66443875", 8) --> "64438756"
revrot("664438769", 8) --> "67834466"
revrot("123456779", 8) --> "23456771"
revrot("", 8) --> ""
revrot("123456779", 0) --> "" 
revrot("563000655734469485", 4) --> "0365065073456944"
Example of a string rotated to the left by one position:
s = "123456" gives "234561".
``` 
```js
// TODO
// 1. Recibir el string, cortarlo en pedazos dependiendo el tamaño que me manden sz
// 2. Desechar o ignorar el sobrante del string si no podemos completar el ultimo chunk con el tamaño requerido en sz
// 3. Si un Chunk representa un entero que sea la suma al cubo de sus numeros si divisible entre 2,
// reversamos ese chunk, caso contrario lo rotamos por una posicion a la izquierda.
// 4. reemsamblamos los chunks juntos en un solo string
  
// if sz is <= 0 or if str is empty return ""
// if sz is greater (>) than the length of str it is impossible to take a chunk of size sz hence return "".
/*
Example of a string rotated to the left by one position:
s = "123456" gives "234561".
*/

//SOLUTION
function revrot(str, sz) {
  if (sz <= 0 || str == "" || sz > str.length) return '';

  let newArray = str.split('');
  let arrayChunks = [];

  while (newArray.length >= sz){
    arrayChunks.push(newArray.splice(0, sz));
  }
  //console.log(arrayChunks); Prueba
  
  let result = arrayChunks.map((eachChunk) => {
    let sum = eachChunk.reduce((prev, curr) => 
      prev + Math.pow(curr, 3),0);
      //console.log(sum); Prueba
      if (sum % 2) {
        //Este es el proceso que se hace cuando el numero es multiplo de 2
        eachChunk.push(eachChunk[0]);
        eachChunk.shift(); //Shift remueve el primer elemento del array y mueve los demas elementos hacia adelante
        return eachChunk.join('');
      } else {
        //se aplica reverse en caso contrario para voltear el arreglo
        return eachChunk.reverse().join(''); 
      }
  });
  return result.join('');
}
```
---------------------------------------------------------------------------------------------------------
Tuesday 10th, May

# *Exercise #1*
## Given the data, define the interface "User" and use it accordingly.

Original Code
```ts
export type User = unknown;

export const users: unknown[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user: unknown) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);
```

Solution
```ts
//Solution
export interface User {  //Aqui se crea el tipo del objeto puede ser type 
    name: string;         // En typeScript tengo que especificar mis variables para objetos
    age : number;         // Si a la variable le pongo age? la hago opcional y si no se llena sera un undefined
    occupation: string;   // si defino el tipo de dato que ingresaria de esta manera string | null quiere decir que puede aceptar un string o null 
}

export const users: User[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user: User) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);

/* In case if you are stuck:

// https://www.typescriptlang.org/docs/handbook/interfaces.html#introduction
*/
```

# *Exercise #2*
## Type "Person" is missing, please define it and use it in persons array and logPerson function in order to fix all the TS errors.

Original code:
```ts
interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = unknown;

export const persons: User[] /* <- Person[] */ = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: User) {
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);
```

Solution:
```ts
interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;  //Agrege | para dejarle saber que el objeto persona puede ser un Admin o un User

export const persons: Person[] /* <- Person[] */ = [  // aqui solo se le agrego que persons va a recibir un arreglo de datos del tipo persona
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: User | Admin) {   // Se agrego que el parametro user puede ser del tipo User or Admin
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);

// In case if you are stuck:
// https://www.typescriptlang.org/docs/handbook/advanced-types.html#union-types
```
    
