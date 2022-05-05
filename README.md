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
