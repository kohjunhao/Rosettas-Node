<img height="128px" width="128px" align="right" />

# Rosetta's Node

> Interesting problems. Quickly described.

<table>
	<thead>
		<tr>
			<th align="center"><strong>Contents</strong></th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>
				<ol>
					<li><a href="#obligatory">Obligatory</a></li>
					<li><a href="#interesting">Interesting</a></li>
					<li><a href="#involved">Involved</a></li>
					<li><a href="#acknowledgements">Acknowledgements</a></li>
					<li><a href="#license">License</a></li>
				</ol>
			</td>
		</tr>
	</tbody>
</table>

<hr>

### Obligatory

These are the problems that have been "done to death". Anything that was once interesting about these problems has since been squashed by their repetition. With that said, this collection wouldn't be complete without them.

<table>
	<thead>
		<tr>
			<th align="center"><strong>Contents</strong></th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>
				<ol>
					<li><a href="#fizzbuzz">FizzBuzz</a></li>
					<li><a href="#fibonacci-iterative">Fibonacci (Iterative)</a></li>
					<li><a href="#fibonacci-recursive">Fibonacci (Recursive)</a></li>
					<li><a href="#palindrome-checker">Palindrome Checker</a></li>
					<li><a href="#leap-year-checker">Leap Year Checker</a></li>
				</ol>
			</td>
		</tr>
	</tbody>
</table>

#### FizzBuzz

-   Print the integers from 1 to 100 (inclusive), but:
    -   for multiples of three, print `"Fizz"` (instead of the number)
    -   for multiples of five, print `"Buzz"` (instead of the number)
    -   for multiples of both three and five, print `"FizzBuzz"` (instead of the number)

**Solution:**

```typescript
for (let i = 1; i <= 10; i++) {
	if (i % 15 === 0) {
		console.log("FizzBuzz");
	} else if (i % 3 === 0) {
		console.log("Fizz");
	} else if (i % 5 === 0) {
		console.log("Buzz");
	} else {
		console.log(i);
	}
}
```

**Sample Output:**

```
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
```

**References:**

-   <http://rosettacode.org/wiki/FizzBuzz>
-   <https://en.wikipedia.org/wiki/Fizz_buzz>

#

#### Fibonacci (Iterative)

-   Print out the `n`th number of the [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_number).
    -   The Fibonacci sequence is the sequence of numbers where each element is the sum of the two previous elements.

**Solution:**

```typescript
function fibonacci(n) {
	const array = [0, 1];

	for (let i = 2; i <= n; i++) {
		array.push(array[i - 2] + array[i - 1]);
	}

	return array[n];
}

console.log(fibonacci(10));
```

**Sample Output:**

```
55
```

**References:**

-   <http://rosettacode.org/wiki/Fibonacci_sequence>
-   <https://en.wikipedia.org/wiki/Fibonacci_number>

#

#### Fibonacci (Recursive)

-   Print out the `n`th number of the [Fibonacci sequence](https://en.wikipedia.org/wiki/Fibonacci_number).
    -   The Fibonacci sequence is the sequence of numbers where each element is the sum of the two previous elements.

**Solution:**

```typescript
function fibonacci(n) {
	if (n < 2) {
		return n;
	}

	return fibonacci(n - 1) + fibonacci(n - 2);
}

console.log(fibonacci(10));
```

**Sample Output:**

```
55
```

**References:**

-   <http://rosettacode.org/wiki/Fibonacci_sequence>
-   <https://en.wikipedia.org/wiki/Fibonacci_number>

#

#### Palindrome Checker

-   Write a function that checks whether a given string is a [palindrome](https://en.wikipedia.org/wiki/Palindrome).
    -   A palindrome is a word or phrase which reads the same backward and forward.

**Solution:**

```typescript
const potentialPalindromes = [
	"Able was I ere I saw Elba.",
	"A man, a plan, a canal – Panama.",
	"Madam, I'm Adam.",
	"Never odd or even.",
	"The quick brown fox jumps over the lazy dog.",
	"Sphinx of black quartz, judge my vow.",
	"How vexingly quick daft zebras jump!",
	"The five boxing wizards jump quickly."
];

function isPalindrome(string) {
	const normalizedString = string.replace(/\W/g, "").toLowerCase();

	return normalizedString === normalizedString.split("").reverse().join("");
}

for (const potentialPalindrome of potentialPalindromes) {
	if (isPalindrome(potentialPalindrome)) {
		console.log("\"" + potentialPalindrome + "\" is a palindrome.");
	} else {
		console.log("\"" + potentialPalindrome + "\" is NOT a palindrome.");
	}
}
```

**Sample Output:**

```
"Able was I ere I saw Elba." is a palindrome.
"A man, a plan, a canal – Panama." is a palindrome.
"Madam, I'm Adam." is a palindrome.
"Never odd or even." is a palindrome.
"The quick brown fox jumps over the lazy dog." is NOT a palindrome.
"Sphinx of black quartz, judge my vow." is NOT a palindrome.
"How vexingly quick daft zebras jump!" is NOT a palindrome.
"The five boxing wizards jump quickly." is NOT a palindrome.
```

**References:**

-   http://rosettacode.org/wiki/Palindrome
-   https://en.wikipedia.org/wiki/Palindrome

#

#### Leap Year Checker

-   Write a function that checks whether a given year is a [leap year](https://en.wikipedia.org/wiki/Leap_year).
    -   A leap year is a year divisible by 4 but not 100 and is not divisible by 400.

**Solution:**

```typescript
function isLeapYear(year) {
    return (year % 100 === 0) ? (year % 400 === 0) : (year % 4 === 0);
};

for (let x = 2010; x <= 2020; x++) {
    if (isLeapYear(x)) {
        console.log(x + " is a leap year.");
    } else {
        console.log(x + " is NOT a leap year.");
    }
}
```

**Sample Output:**

```
2010 is NOT a leap year.
2011 is NOT a leap year.
2012 is a leap year.
2013 is NOT a leap year.
2014 is NOT a leap year.
2015 is NOT a leap year.
2016 is a leap year.
2017 is NOT a leap year.
2018 is NOT a leap year.
2019 is NOT a leap year.
2020 is a leap year.
```

**References:**

-   http://rosettacode.org/wiki/Leap_year
-   https://en.wikipedia.org/wiki/Leap_year

<hr>

### Interesting

<table>
	<thead>
		<tr>
			<th align="center"><strong>Contents</strong></th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>
				<ol>
					<li><a href="#abbreviations">Abbreviations</a></li>
					<li><a href="#letter-blocks">Letter Blocks</a></li>
					<li><a href="#align-columns">Align Columns</a></li>
					<li><a href="#almost-prime">Almost Prime</a></li>
					<li><a href="#balanced-brackets">Balanced Brackets</a></li>
					<li><a href="#caesar-cipher">Caesar Cipher</a></li>
					<li><a href="#caesar-cipher-solver">Caesar Cipher Solver</a></li>
					<li><a href="#calendar">Calendar</a></li>
					<li><a href="#chaocipher">Chaocipher</a></li>
					<li><a href="#recursion-limit">Recursion Limit</a></li>
					<li><a href="#history-variables">History Variables</a></li>
					<li><a href="#last-letter-first-letter">Last Letter-First Letter</a></li>
					<li><a href="#linear-congruential-generator">Linear Congruential Generator</a></li>
					<li><a href="#ordered-words">Ordered Words</a></li>
					<li><a href="#pangram-checker">Pangram Checker</a></li>
					<li><a href="#pascals-triangle">Pascal's Triangle</a></li>
					<li><a href="#pascals-triangle-puzzle">Pascal's Triangle Puzzle</a></li>
					<li><a href="#international-bank-account-number-iban-validator">International Bank Account Number (IBAN) Validator</a></li>
					<li><a href="#luhn-algorithm">Luhn Algorithm</a></li>
					<li><a href="#maximum-triangle-path-sum">Maximum Triangle Path Sum</a></li>
					<li><a href="#poker-hand-analyzer">Poker Hand Analyzer</a></li>
					<li><a href="#perfect-shuffle">Perfect Shuffle</a></li>
					<li><a href="#quine">Quine</a></li>
					<li><a href="#remove-duplicate-elements">Remove Duplicate Elements</a></li>
					<li><a href="#semordnilap">Semordnilap</a></li>
					<li><a href="#sparkline">Sparkline</a></li>
					<li><a href="#textonyms">Textonyms</a></li>
					<li><a href="#towers-of-hanoi">Towers of Hanoi</a></li>
					<li><a href="#truth-tables">Truth Tables</a></li>
					<li><a href="#ulam-spiral">Ulam spiral</a></li>
					<li><a href="#vigenre-cipher">Vigenère cipher</a></li>
					<li><a href="#visualize-a-tree">Visualize a Tree</a></li>
					<li><a href="#water-collected-between-towers">Water Collected Between Towers</a></li>
					<li><a href="#word-search-generator">Word Search Generator</a></li>
					<li><a href="#word-search-solver">Word Search Solver</a></li>
					<li><a href="#word-wrap">Word Wrap</a></li>
				</ol>
			</td>
		</tr>
	</tbody>
</table>

#### Abbreviations

-   Write a function to find the minimum, _fixed-length_ abbreviation for an array that would preserve each element's uniqueness.

**Solution:**

```typescript
const arrays = [
	["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"],
	["Domingo", "Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado"],
	["dimanche", "Lundi", "Mardi", "Mercredi", "Jeudi", "Vendredi", "Samedi"],
	["domenica", "lunedì", "martedì", "mercoledì", "giovedì", "venerdì", "sabato"],
	["duminica", "luni", "marti", "miercuri", "joi", "vineri", "sambata"]
];

function getMinimumLengthUniqueAbbreviations(array) {
	const longestStringLength = array.sort(function(a, b) { return b.length - a.length; })[0].length;

	for (let x = longestStringLength; x >= 1; x--) {
		let tempObject = {};

		for (let string of array) {
			tempObject[string.substring(0, x)] = undefined;
		}

		if (Object.keys(tempObject).length === array.length) {
			array = Object.keys(tempObject);
		}
	}

	return array;
}

for (const array of arrays) {
	console.log("[\"" + array.join("\", \"") + "\"] can be abbreviated to [\"" + getMinimumLengthUniqueAbbreviations(array).join("\", \"") + "\"]");
}
```

**Sample Output:**

```
["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"] can be abbreviated to ["We", "Th", "Sa", "Tu", "Su", "Mo", "Fr"]
["Domingo", "Lunes", "Martes", "Miércoles", "Jueves", "Viernes", "Sábado"] can be abbreviated to ["Mi", "Do", "Vi", "Ma", "Ju", "Sá", "Lu"]
["dimanche", "Lundi", "Mardi", "Mercredi", "Jeudi", "Vendredi", "Samedi"] can be abbreviated to ["di", "Me", "Ve", "Sa", "Lu", "Ma", "Je"]
["domenica", "lunedì", "martedì", "mercoledì", "giovedì", "venerdì", "sabato"] can be abbreviated to ["me", "do", "ma", "gi", "ve", "lu", "sa"]
["duminica", "luni", "marti", "miercuri", "joi", "vineri", "sambata"] can be abbreviated to ["du", "mi", "sa", "vi", "ma", "lu", "jo"]
```

**Variants:**

-   Produce an array of minimal-length strings instead of fixed-length strings.

**References:**

-   <http://rosettacode.org/wiki/Abbreviations,_automatic>

#

#### Letter Blocks

-   Write a function that determines whether a word can be spelled with a given collection of blocks.
-   Blocks are guaranteed to have the same letter pairs on them.

**Solution:**

```typescript
const blocks = [
	["B", "O"],
	["X", "K"],
	["D", "Q"],
	["C", "P"],
	["N", "A"],
	["G", "T"],
	["R", "E"],
	["T", "G"],
	["Q", "D"],
	["F", "S"],
	["J", "W"],
	["H", "U"],
	["V", "I"],
	["A", "N"],
	["O", "B"],
	["E", "R"],
	["F", "S"],
	["L", "Y"],
	["P", "C"],
	["Z", "M"]
];

const words = [
	"A",
	"BARK",
	"BOOK",
	"TREAT",
	"COMMON",
	"SQUAD",
	"CONFUSE"
];

function isWordSpellableWithBlocks(word, blocks) {
	for (const letter of word) {
		let letterFound = false;

		for (const [index, block] of blocks.entries()) {
			if (block[0] === letter || block[1] === letter) {
				blocks[index] = ["", ""];
				letterFound = true;
				break;
			}
		}

		if (letterFound === false) {
			return false;
		}
	}

	return true;
}

for (const word of words) {
	if (isWordSpellableWithBlocks(word, [...blocks])) {
		console.log("The word \"" + word + "\" can be spelled with these blocks.");
	} else {
		console.log("The word \"" + word + "\" can NOT be spelled with these blocks.");
	}
}
```

**Sample Output:**

```
The word "A" can be spelled with these blocks.
The word "BARK" can be spelled with these blocks.
The word "BOOK" can NOT be spelled with these blocks.
The word "TREAT" can be spelled with these blocks.
The word "COMMON" can NOT be spelled with these blocks.
The word "SQUAD" can be spelled with these blocks.
The word "CONFUSE" can be spelled with these blocks.
```

**Variants:**

-   Blocks are not guaranteed to have the same letter pairs on them.

**References:**

-   http://rosettacode.org/wiki/ABC_Problem

#

#### Align Columns

-

**Solution:**

```typescript
const input = [
	"Given a multiline input string, where the words within a line".split(" "),
	"are delineated by a single space character, write a program".split(" "),
	"that aligns each column of words by ensuring that the words in".split(" "),
	"each column are separated by at least one space.".split(" "),
	"Further, allow for each word in a column to be either left".split(" "),
	"justified, right justified, or center justified within its column.".split(" ")
];

function getLongestRow(input) {
	let longestRow = 0;

	for (const row of input) {
		if (row.length > longestRow) {
			longestRow = row.length;
		}
	}

	return longestRow;
}

function alignLeft(input) {
	const longestRow = getLongestRow(input);

}

function alignRight(input) {
	const longestRow = getLongestRow(input);

}

function alignCenter(input) {
	const longestRow = getLongestRow(input);

}

console.log("Left:");
console.log(alignLeft(input));

console.log("Right:");
console.log(alignRight(input));

console.log("Center:");
console.log(alignCenter(input));
```

**Sample Output:**

```
```

**References:**

-

#

#### Almost Prime

-

**Solution:**

```typescript
//@import "./almostPrime.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Balanced Brackets

-

**Solution:**

```typescript
//@import "./balancedBrackets.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Caesar Cipher

-

**Solution:**

```typescript
//@import "./caesarCipher.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Caesar Cipher Solver

-

**Solution:**

```typescript
//@import "./caesarCipherSolver.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Calendar

-

**Solution:**

```typescript
//@import "./calendar.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Chaocipher

-

**Solution:**

```typescript
//@import "./chaocipher.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Recursion Limit

-

**Solution:**

```typescript
//@import "./recursionLimit.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### History Variables

-

**Solution:**

```typescript
//@import "./historyVariables.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Last Letter-First Letter

-

**Solution:**

```typescript
//@import "./lastLetterFirstLetter.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Linear Congruential Generator

-

**Solution:**

```typescript
//@import "./linearCongruentialGenerator.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Ordered Words

-

**Solution:**

```typescript
//@import "./orderedWords.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Pangram Checker

-

**Solution:**

```typescript
//@import "./pangramChecker.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Pascal's Triangle

-

**Solution:**

```typescript
//@import "./pangramChecker.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Pascal's Triangle Puzzle

-

**Solution:**

```typescript
//@import "./pangramChecker.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### International Bank Account Number (IBAN) Validator

-

**Solution:**

```typescript
//@import "./ibanValidator.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Luhn Algorithm

-

**Solution:**

```typescript
//@import "./luhnAlgorithm.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Maximum Triangle Path Sum

-

**Solution:**

```typescript
//@import "./maximumTrianglePathSum.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Poker Hand Analyzer

-

**Solution:**

```typescript
//@import "./pokerHandAnalyzer.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Perfect Shuffle

-

**Solution:**

```typescript
//@import "./perfectShuffle.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Quine

-

**Solution:**

```typescript
//@import "./quine.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Remove Duplicate Elements

-

**Solution:**

```typescript
//@import "./removeDuplicateElements.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Semordnilap

-

**Solution:**

```typescript
//@import "./semordnilap.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Sparkline

-

**Solution:**

```typescript
//@import "./sparkline.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Textonyms

-

**Solution:**

```typescript
//@import "./textonyms.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Towers of Hanoi

-

**Solution:**

```typescript
//@import "./textonyms.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Truth Tables

-

**Solution:**

```typescript
//@import "./truthTables.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Ulam spiral

-

**Solution:**

```typescript
//@import "./ulamSpiral.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Vigenère cipher

-

**Solution:**

```typescript
//@import "./vigenereCipher.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Visualize a Tree

-

**Solution:**

```typescript
//@import "./visualizeATree.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Water Collected Between Towers

-

**Solution:**

```typescript
//@import "./visualizeATree.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Word Search Generator

-

**Solution:**

```typescript
//@import "./wordSearchGenerator.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Word Search Solver

-

**Solution:**

```typescript
//@import "./wordSearchSolver.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Word Wrap

-

**Solution:**

```typescript
//@import "./wordWrap.ts";
```

**Sample Output:**

```
```

**References:**

-

#

<hr>

### Involved

<table>
	<thead>
		<tr>
			<th align="center"><strong>Contents</strong></th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>
				<ol>
					<li><a href="#abelian-sandpile-model">Abelian Sandpile Model</a></li>
					<li><a href="#conways-game-of-life">Conway's Game of Life</a></li>
					<li><a href="#dijkstras-algorithm">Dijkstra's Algorithm</a></li>
					<li><a href="#dinesmans-multiple-dwelling-problem">Dinesman's Multiple-dwelling Problem</a></li>
					<li><a href="#dining-philosophers">Dining Philosophers</a></li>
					<li><a href="#discordian-date">Discordian Date</a></li>
					<li><a href="#egyptian-division">Egyptian Division</a></li>
					<li><a href="#egyptian-fractions">Egyptian Fractions</a></li>
					<li><a href="#evolutionary-algorithm">Evolutionary Algorithm</a></li>
					<li><a href="#markov-algorithm">Markov Algorithm</a></li>
					<li><a href="#forest-fire">Forest Fire</a></li>
					<li><a href="#galton-box-animation">Galton Box Animation</a></li>
					<li><a href="#chess960-starting-positions">Chess960 Starting Positions</a></li>
					<li><a href="#random-chess-positions">Random Chess Positions</a></li>
					<li><a href="#huffman-encoding">Huffman Encoding</a></li>
					<li><a href="#hunt-the-wumpus">Hunt the Wumpus</a></li>
					<li><a href="#inverted-index">Inverted Index</a></li>
					<li><a href="#jaro-distance">Jaro Distance</a></li>
					<li><a href="#josephus-problem">Josephus Problem</a></li>
					<li><a href="#knapsack-problem">Knapsack Problem</a></li>
					<li><a href="#knights-tour">Knight's Tour</a></li>
					<li><a href="#langtons-ant">Langton's Ant</a></li>
					<li><a href="#levenshtein-distance">Levenshtein Distance</a></li>
					<li><a href="#longest-common-subsequence">Longest Common Subsequence</a></li>
					<li><a href="#longest-common-substring">Longest Common Substring</a></li>
					<li><a href="#mayan-numerals">Mayan Numerals</a></li>
					<li><a href="#maze-generator">Maze Generator</a></li>
					<li><a href="#maze-solver">Maze Solver</a></li>
					<li><a href="#metered-concurrency">Metered Concurrency</a></li>
					<li><a href="#mind-boggling-card-trick">Mind-Boggling Card Trick</a></li>
					<li><a href="#minesweeper">Minesweeper</a></li>
					<li><a href="#monte-carlo-method">Monte Carlo Method</a></li>
					<li><a href="#monte-hall-problem">Monte Hall Problem</a></li>
					<li><a href="#morse-code">Morse Code</a></li>
					<li><a href="#move-to-front-algorithm">Move-to-front Algorithm</a></li>
					<li><a href="#n-queens-problem">N-queens Problem</a></li>
					<li><a href="#rpn-calculator-algorithm">RPN Calculator Algorithm</a></li>
					<li><a href="#rpn-to-infix-converter">RPN to Infix Converter</a></li>
					<li><a href="#shunting-yard-algorithm">Shunting Yard Algorithm</a></li>
					<li><a href="#password-generator">Password Generator</a></li>
					<li><a href="#sokoban">Sokoban</a></li>
					<li><a href="#straddling-checkerboard">Straddling Checkerboard</a></li>
					<li><a href="#sudoku-generator">Sudoku Generator</a></li>
					<li><a href="#sudoku-solver">Sudoku Solver</a></li>
				</ol>
			</td>
		</tr>
	</tbody>
</table>

#### Abelian Sandpile Model

-

**Solution:**

```typescript
//@import "./abelianSandpile.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Conway's Game of Life

-

**Solution:**

```typescript
//@import "./gameOfLife.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Dijkstra's Algorithm

-

**Solution:**

```typescript
//@import "./dijkstrasAlgorithm.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Dinesman's Multiple-dwelling Problem

-

**Solution:**

```typescript
//@import "./dinemansProblem.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Dining Philosophers

-

**Solution:**

```typescript
//@import "./diningPhilosophers.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Discordian Date

-

**Solution:**

```typescript
//@import "./discordianDate.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Egyptian Division

-

**Solution:**

```typescript
//@import "./egyptianDivision.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Egyptian Fractions

-

**Solution:**

```typescript
//@import "./egyptianFractions.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Evolutionary Algorithm

-

**Solution:**

```typescript
//@import "./evolutionaryAlgorithm.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Markov Algorithm

-

**Solution:**

```typescript
//@import "./markovAlgorithm.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Forest Fire

-

**Solution:**

```typescript
//@import "./pangramChecker.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Galton Box Animation

-

**Solution:**

```typescript
//@import "./galtonBox.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Chess960 Starting Positions

-

**Solution:**

```typescript
//@import "./chess960.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Random Chess Positions

-

**Solution:**

```typescript
//@import "./randomChessPositions.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Huffman Encoding

-

**Solution:**

```typescript
//@import "./huffmanEncoding.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Hunt the Wumpus

-

**Solution:**

```typescript
//@import "./huntTheWumpus.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Inverted Index

-

**Solution:**

```typescript
//@import "./invertedIndex.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Jaro Distance

-

**Solution:**

```typescript
//@import "./jaroDistance.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Josephus Problem

-

**Solution:**

```typescript
//@import "./josephusProblem.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Knapsack Problem

-

**Solution:**

```typescript
//@import "./knapsackProblem.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Knight's Tour

-

**Solution:**

```typescript
//@import "./knightsTour.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Langton's Ant

-

**Solution:**

```typescript
//@import "./langtonsAnt.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Levenshtein Distance

-

**Solution:**

```typescript
//@import "./levenshteinDistance.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Longest Common Subsequence

-

**Solution:**

```typescript
//@import "./longestCommonSubsequence.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Longest Common Substring

-

**Solution:**

```typescript
//@import "./longestCommonSubstring.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Mayan Numerals

-

**Solution:**

```typescript
//@import "./maximumTrianglePathSum.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Maze Generator

-

**Solution:**

```typescript
//@import "./mazeGenerator.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Maze Solver

-

**Solution:**

```typescript
//@import "./mazeSolver.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Metered Concurrency

-

**Solution:**

```typescript
//@import "./meteredConcurrency.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Mind-Boggling Card Trick

-

**Solution:**

```typescript
//@import "./mindBogglingCardTrick.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Minesweeper

-

**Solution:**

```typescript
//@import "./minesweeper.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Monte Carlo Method

-

**Solution:**

```typescript
//@import "./monteCarloMethod.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Monte Hall Problem

-

**Solution:**

```typescript
//@import "./monteHallProblem.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Morse Code

-

**Solution:**

```typescript
//@import "./morseCode.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Move-to-front Algorithm

-

**Solution:**

```typescript
//@import "./moveToFrontAlgorithm.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### N-queens Problem

-

**Solution:**

```typescript
//@import "./nQueensProblem.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### RPN Calculator Algorithm

-

**Solution:**

```typescript
//@import "./rpnCalculatorAlgorithm.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### RPN to Infix Converter

-

**Solution:**

```typescript
//@import "./rpnToInfixConverter.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Shunting Yard Algorithm

-

**Solution:**

```typescript
//@import "./shuntingYardAlgorithm.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Password Generator

-

**Solution:**

```typescript
//@import "./passwordGenerator.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Sokoban

-

**Solution:**

```typescript
//@import "./sokoban.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Straddling Checkerboard

-

**Solution:**

```typescript
//@import "./straddlingCheckerboard.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Sudoku Generator

-

**Solution:**

```typescript
//@import "./sudokuGenerator.ts";
```

**Sample Output:**

```
```

**References:**

-

#

#### Sudoku Solver

-

**Solution:**

```typescript
//@import "./sudokuSolver.ts";
```

**Sample Output:**

```
```

**References:**

-

#

<hr>

### Acknowledgements

-   [Rosetta Code](http://rosettacode.org/wiki/Rosetta_Code)

### License

`Rosettas-Node` is licensed under the [MIT License](https://github.com/brianjenkins94/Rosettas-Node/blob/master/LICENSE).

All files located in the `node_modules` directory are externally maintained libraries used by this software which have their own licenses; it is recommend that you read them, as their terms may differ from the terms in the MIT License.
