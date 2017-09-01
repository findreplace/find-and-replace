# Find and Replace Text Online

[Find and Replace](https://findreplace.net/) is a free online tool that allows you to easily search for a letter, number, word, or phrase in your text document and substitute it with something else. It can be very useful when it comes to editing a huge chunk of text. This tool will automatically find all exact matches and replace them all in a single click of a button.

## Usage
Find & Replace is pretty straightforward to use.
1. First, fill the "Find this" field with the word you want to change and the "Replace with" field with the new word you want to use.
2. Next, paste your text in the text box. Alternatively, you can click the "Open File" button in the menu bar to directly load a file from 3. your computer. See supported file extensions below.
4. Lastly, click the "Replace All" button to start the process.

## Options
* Global - Global match is used to replace all occurrences of the word you're searching for in the text document. When disabled, the search and replace operation will stop after the first match.
* Match case - By default, the tool will replace all occurence of the string you're searching for regardless of the letter case. Enable this to make the operation case sensitive to exactly match search query.
* Words Only - Replace a match if it's not preceeded or followed by another string. For example, searching "back" does not match the "back" in the word "backwards".
* RegEx - Allows you to use Regular Expressions.
* Multiline - Adds Regular Expressions m modifier to perform multi-line matching

## Regular Expressions
Find & Replace gives you an option to use Regular Expressions to perform a more complex type of search and replace operations. Below is a list of basic examples that you can use as a cheat sheet.

### Basic Examples
Using the or condition to search for multiple words.
* Input: `one two three`
* Find: `one|two|three` and Replace with: ``number`
* Result: `number number number`

### Switching the positions of the words.
* Input: `hello world`
* Find: `(hello) (world)` and Replace with: `$2 $1`
* Result: `world hello`

### Wrapping a word.
* Input: `This is a sample text`
* Find: `(sample)` and Replace with: `<b>$1</b>`
* Result: `This is a <b>sample</b> text`

### Replace only if followed by certain characters.
* Input: `upgrade`
* Find: `up(?=grade)` and Replace with: `down`
* Result: `downgrade`

It will not match the "up" in the word "update" since it is not followed by "grade".

Note: For negation, simply replace `=` with `!`

### Matching an unknown number.
* Input: `width="356"`
* Find: `width="([0-9]+)"` and Replace with: `width="100%"`
* Result: `width="100%"`

### Special characters
You must place a backslash '\' before a special character. The tool will generate an error message that says: "SyntaxError: Invalid regular expression: / . ^ $ * + ? \ [ ( { |/: Unterminated character class" if you have forgotten to escape the backslash .

For example, to match Where? use Where\? - the \? is taken to mean ?.
* Input: `Where?`
* Find: `Where\?` and Replace with: `What?`
* Result: `What?`
