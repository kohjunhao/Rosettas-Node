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
for (let i = 1; i <= 100; i++) {
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
1⏎ 2⏎ Fizz⏎ 4⏎ Buzz⏎ Fizz⏎ 7⏎ 8⏎ Fizz⏎ Buzz⏎ 11⏎ Fizz⏎ 13⏎ 14⏎ FizzBuzz⏎ 16⏎ 17⏎ Fizz⏎ 19⏎ Buzz⏎ Fizz⏎ 22⏎ 23⏎ Fizz⏎ Buzz⏎ 26⏎ Fizz⏎ 28⏎ 29⏎ FizzBuzz⏎ 31⏎ 32⏎ Fizz⏎ 34⏎ Buzz⏎ Fizz⏎ 37⏎ 38⏎ Fizz⏎ Buzz⏎ 41⏎ Fizz⏎ 43⏎ 44⏎ FizzBuzz⏎ 46⏎ 47⏎ Fizz⏎ 49⏎ Buzz⏎ Fizz⏎ 52⏎ 53⏎ Fizz⏎ Buzz⏎ 56⏎ Fizz⏎ 58⏎ 59⏎ FizzBuzz⏎ 61⏎ 62⏎ Fizz⏎ 64⏎ Buzz⏎ Fizz⏎ 67⏎ 68⏎ Fizz⏎ Buzz⏎ 71⏎ Fizz⏎ 73⏎ 74⏎ FizzBuzz⏎ 76⏎ 77⏎ Fizz⏎ 79⏎ Buzz⏎ Fizz⏎ 82⏎ 83⏎ Fizz⏎ Buzz⏎ 86⏎ Fizz⏎ 88⏎ 89⏎ FizzBuzz⏎ 91⏎ 92⏎ Fizz⏎ 94⏎ Buzz⏎ Fizz⏎ 97⏎ 98⏎ Fizz⏎ Buzz
```

**References:**

-   <http://rosettacode.org/wiki/FizzBuzz>
-   <https://en.wikipedia.org/wiki/Fizz_buzz>

#### Fibonacci (Iterative)

-   Print out the `n`th number of the Fibonacci sequence.
    -   The Fibonacci sequence is the sequence of numbers where each element is the sum of the two previous elements.

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

#### Fibonacci (Recursive)

-   Print out the `n`th number of the Fibonacci sequence.
    -   The Fibonacci sequence is the sequence of numbers where each element is the sum of the two previous elements.

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

#### Palindrome Checker

```typescript
//@import "./palindromeChecker.ts";
```

#### Leap Year Checker

```typescript
//@import "./leapYearChecker.ts";
```

<hr>

### Interesting

<hr>

### Involved

<hr>

### Acknowledgements

-   [Rosetta Code](http://rosettacode.org/wiki/Rosetta_Code)

### License

`Rosettas-Node` is licensed under the [MIT License](https://github.com/brianjenkins94/Rosettas-Node/blob/master/LICENSE).

All files located in the `node_modules` directory are externally maintained libraries used by this software which have their own licenses; it is recommend that you read them, as their terms may differ from the terms in the MIT License.
