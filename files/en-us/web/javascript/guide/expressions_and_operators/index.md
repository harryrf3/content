---
title: Expressions and operators
slug: Web/JavaScript/Guide/Expressions_and_Operators
tags:
  - Beginner
  - Expressions
  - Guide
  - JavaScript
  - Operators
  - 'l10n:priority'
---
<div>{{jsSidebar("JavaScript Guide")}} {{PreviousNext("Web/JavaScript/Guide/Functions",
  "Web/JavaScript/Guide/Numbers_and_dates")}}</div>

<p class="summary">This chapter describes JavaScript's expressions and operators,
  including assignment, comparison, arithmetic, bitwise, logical, string, ternary and
  more.</p>

<p>A complete and detailed list of operators and expressions is also available in the <a
    href="/en-US/docs/Web/JavaScript/Reference/Operators">reference</a>.</p>

<h2 id="Operators">Operators</h2>

<p>JavaScript has the following types of operators. This section describes the operators
  and contains information about operator precedence.</p>

<ul>
 <li><a href="#assignment_operators">Assignment operators</a></li>
 <li><a href="#comparison_operators">Comparison operators</a></li>
 <li><a href="#arithmetic_operators">Arithmetic operators</a></li>
 <li><a href="#bitwise_operators">Bitwise operators</a></li>
 <li><a href="#logical_operators">Logical operators</a></li>
 <li><a href="#string_operators">String operators</a></li>
 <li><a href="#conditional_ternary_operator">Conditional (ternary) operator</a></li>
 <li><a href="#comma_operator">Comma operator</a></li>
 <li><a href="#unary_operators">Unary operators</a></li>
 <li><a href="#relational_operators">Relational operators</a></li>
</ul>

<p>JavaScript has both <em>binary</em> and <em>unary</em> operators, and one special
  ternary operator, the conditional operator. A binary operator requires two operands, one
  before the operator and one after the operator:</p>

<pre class="brush: js"><em>operand1</em> <em>operator</em> <em>operand2</em>
</pre>

<p>For example, <code>3+4</code> or <code>x*y</code>.</p>

<p>A unary operator requires a single operand, either before or after the operator:</p>

<pre class="brush: js"><em>operator</em> <em>operand</em>
</pre>

<p>or</p>

<pre class="brush: js"><em>operand</em> <em>operator</em>
</pre>

<p>For example, <code>x++</code> or <code>++x</code>.</p>

<h3 id="Assignment_operators">Assignment operators</h3>

<p>An assignment operator assigns a value to its left operand based on the value of its
  right operand. The simple assignment operator is equal (<code>=</code>), which assigns
  the value of its right operand to its left operand. That is, <code>x = y</code> assigns
  the value of <code>y</code> to <code>x</code>.</p>

<p>There are also compound assignment operators that are shorthand for the operations
  listed in the following table:</p>

<table class="standard-table">
  <caption>Compound assignment operators</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Shorthand operator</th>
      <th>Meaning</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Assignment">Assignment</a>
      </td>
      <td><code>x = y</code></td>
      <td><code>x = y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Addition_assignment">Addition
          assignment</a></td>
      <td><code>x += y</code></td>
      <td><code>x = x + y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Subtraction_assignment">Subtraction
          assignment</a></td>
      <td><code>x -= y</code></td>
      <td><code>x = x - y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Multiplication_assignment">Multiplication
          assignment</a></td>
      <td><code>x *= y</code></td>
      <td><code>x = x * y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Division_assignment">Division
          assignment</a></td>
      <td><code>x /= y</code></td>
      <td><code>x = x / y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Remainder_assignment">Remainder
          assignment</a></td>
      <td><code>x %= y</code></td>
      <td><code>x = x % y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Exponentiation_assignment">Exponentiation
          assignment</a></td>
      <td><code>x **= y</code></td>
      <td><code>x = x ** y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Left_shift_assignment">Left
          shift assignment</a></td>
      <td><code>x &lt;&lt;= y</code></td>
      <td><code>x = x &lt;&lt; y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Right_shift_assignment">Right
          shift assignment</a></td>
      <td><code>x &gt;&gt;= y</code></td>
      <td><code>x = x &gt;&gt; y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Unsigned_right_shift_assignment">Unsigned
          right shift assignment</a></td>
      <td><code>x &gt;&gt;&gt;= y</code></td>
      <td><code>x = x &gt;&gt;&gt; y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_AND_assignment">Bitwise
          AND assignment</a></td>
      <td><code>x &amp;= y</code></td>
      <td><code>x = x &amp; y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_XOR_assignment">Bitwise
          XOR assignment</a></td>
      <td><code>x ^= y</code></td>
      <td><code>x = x ^ y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_OR_assignment">Bitwise
          OR assignment</a></td>
      <td><code>x |= y</code></td>
      <td><code>x = x | y</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND_assignment">Logical
          AND assignment</a></td>
      <td><code>x &amp;&amp;= y</code></td>
      <td><code>x &amp;&amp; (x = y)</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Logical_OR_assignment">Logical
          OR assignment</a></td>
      <td><code>x ||= y</code></td>
      <td><code>x || (x = y)</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Logical_nullish_assignment">Logical
          nullish assignment</a></td>
      <td><code>x ??= y</code></td>
      <td><code>x ?? (x = y)</code></td>
    </tr>
  </tbody>
</table>

<h4 id="Return_value_and_chaining">Return value and chaining</h4>

<p>Like most expressions, assignments like <code>x = y</code> have a return value. It can
  be retrieved by e.g. assigning the expression or logging it:</p>

<pre>const z = (x = y); // Or equivalently: const z = x = y;

console.log(z); // Log the return value of the assignment x = y.
console.log(x = y); // Or log the return value directly.
</pre>

<p>The return value matches the expression to the right of the <code>=</code> sign in the
  “Meaning” column of the table above. That means that <code>(x = y)</code> returns
  <code>y</code>, <code>(x += y)</code> returns the resulting sum <code>x + y</code>,
  <code>(x **= y)</code> returns the resulting power <code>x ** y</code>, and so on.</p>

<p>In the case of logical assignments, <code>(x &amp;&amp;= y)</code>,
  <code>(x ||= y)</code>, and <code>(x ??= y)</code>, the return value is that of the
  logical operation without the assignment, so <code>x &amp;&amp; y</code>,
  <code>x || y</code>, and <code>x ?? y</code>, respectively.</p>

<p>Note that the return values are always based on the operands’ values <em>before</em>
  the operation.</p>

<p>When chaining these expressions, each assignment is evaluated
  <strong>right-to-left</strong>. Consider these examples:</p>

<ul>
  <li><code>w = z = x = y</code> is equivalent to <code>w = (z = (x = y))</code> or
    <code>x = y; z = y; w = y</code></li>
  <li><code>z += x *= y</code> is equivalent to <code>z += (x *= y)</code> or
    <code>tmp = x * y; x *= y; z += tmp</code> (except without the <code>tmp</code>).</li>
</ul>

<h4 id="Destructuring">Destructuring</h4>

<p>For more complex assignments, the <a
    href="/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment">destructuring
    assignment</a> syntax is a JavaScript expression that makes it possible to extract
  data from arrays or objects using a syntax that mirrors the construction of array and
  object literals.</p>

<pre class="brush: js">var foo = ['one', 'two', 'three'];

// without destructuring
var one   = foo[0];
var two   = foo[1];
var three = foo[2];

// with destructuring
var [one, two, three] = foo;</pre>

<h3 id="Comparison_operators">Comparison operators</h3>

<p>A comparison operator compares its operands and returns a logical value based on
  whether the comparison is true. The operands can be numerical, string, logical, or
  object values. Strings are compared based on standard lexicographical ordering, using
  Unicode values. In most cases, if the two operands are not of the same type, JavaScript
  attempts to convert them to an appropriate type for the comparison. This behavior
  generally results in comparing the operands numerically. The sole exceptions to type
  conversion within comparisons involve the <code>===</code> and <code>!==</code>
  operators, which perform strict equality and inequality comparisons. These operators do
  not attempt to convert the operands to compatible types before checking equality. The
  following table describes the comparison operators in terms of this sample code:</p>

<pre class="brush: js">var var1 = 3;
var var2 = 4;
</pre>

<table class="standard-table">
  <caption>Comparison operators</caption>
  <thead>
    <tr>
      <th scope="col">Operator</th>
      <th scope="col">Description</th>
      <th scope="col">Examples returning true</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators#equality">Equal</a>
        (<code>==</code>)</td>
      <td>Returns <code>true</code> if the operands are equal.</td>
      <td><code>3 == var1</code>
        <p><code>"3" == var1</code></p>
        <code>3 == '3'</code>
      </td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators#inequality">
          Not equal</a> (<code>!=</code>)
      </td>
      <td>Returns <code>true</code> if the operands are not equal.</td>
      <td><code>var1 != 4<br>
    var2 != "3"</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators#identity">Strict
          equal</a> (<code>===</code>)</td>
      <td>Returns <code>true</code> if the operands are equal and of the same type. See
        also {{jsxref("Object.is")}} and <a
          href="/en-US/docs/Web/JavaScript/Equality_comparisons_and_sameness">sameness in
          JS</a>.</td>
      <td><code>3 === var1</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators#nonidentity">Strict
          not equal</a> (<code>!==</code>)</td>
      <td>Returns <code>true</code> if the operands are of the same type but not equal, or
        are of different type.</td>
      <td><code>var1 !== "3"<br>
    3 !== '3'</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators#greater_than_operator">Greater
          than</a> (<code>&gt;</code>)</td>
      <td>Returns <code>true</code> if the left operand is greater than the right operand.
      </td>
      <td><code>var2 &gt; var1<br>
    "12" &gt; 2</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators#greater_than_or_equal_operator">Greater
          than or equal</a> (<code>&gt;=</code>)</td>
      <td>Returns <code>true</code> if the left operand is greater than or equal to the
        right operand.</td>
      <td><code>var2 &gt;= var1<br>
    var1 &gt;= 3</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators#less_than_operator">Less
          than</a> (<code>&lt;</code>)</td>
      <td>Returns <code>true</code> if the left operand is less than the right operand.
      </td>
      <td><code>var1 &lt; var2<br>
    "2" &lt; 12</code></td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators#less_than_or_equal_operator">Less
          than or equal</a> (<code>&lt;=</code>)</td>
      <td>Returns <code>true</code> if the left operand is less than or equal to the right
        operand.</td>
      <td><code>var1 &lt;= var2<br>
    var2 &lt;= 5</code></td>
    </tr>
  </tbody>
</table>

<div class="note">
  <p><strong>Note:</strong> <code>=&gt;</code> is not an operator, but the notation
    for <a href="/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions">Arrow
      functions</a>.</p>
</div>

<h3 id="Arithmetic_operators">Arithmetic operators</h3>

<p>An arithmetic operator takes numerical values (either literals or variables) as their
  operands and returns a single numerical value. The standard arithmetic operators are
  addition (<code>+</code>), subtraction (<code>-</code>), multiplication
  (<code>*</code>), and division (<code>/</code>). These operators work as they do in most
  other programming languages when used with floating point numbers (in particular, note
  that division by zero produces {{jsxref("Infinity")}}). For example:</p>

<pre class="brush: js">1 / 2; // 0.5
1 / 2 == 1.0 / 2.0; // this is true
</pre>

<p>In addition to the standard arithmetic operations (<code>+</code>, <code>-</code>,
  <code>*</code>, <code>/</code>), JavaScript provides the arithmetic operators listed in
  the following table:</p>

<table class="fullwidth-table">
  <caption>Arithmetic operators</caption>
  <thead>
    <tr>
      <th scope="col">Operator</th>
      <th scope="col">Description</th>
      <th scope="col">Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Remainder">Remainder</a>
        (<code>%</code>)</td>
      <td>Binary operator. Returns the integer remainder of dividing the two operands.
      </td>
      <td>12 % 5 returns 2.</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Increment">Increment</a>
        (<code>++</code>)</td>
      <td>Unary operator. Adds one to its operand. If used as a prefix operator
        (<code>++x</code>), returns the value of its operand after adding one; if used as
        a postfix operator (<code>x++</code>), returns the value of its operand before
        adding one.</td>
      <td>If <code>x</code> is 3, then <code>++x</code> sets <code>x</code> to 4 and
        returns 4, whereas <code>x++</code> returns 3 and, only then, sets <code>x</code>
        to 4.</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Decrement">Decrement</a>
        (<code>--</code>)</td>
      <td>Unary operator. Subtracts one from its operand. The return value is analogous to
        that for the increment operator.</td>
      <td>If <code>x</code> is 3, then <code>--x</code> sets <code>x</code> to 2 and
        returns 2, whereas <code>x--</code> returns 3 and, only then, sets <code>x</code>
        to 2.</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Unary_negation">Unary
          negation</a> (<code>-</code>)</td>
      <td>Unary operator. Returns the negation of its operand.</td>
      <td>If <code>x</code> is 3, then <code>-x</code> returns -3.</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Unary_plus">Unary
          plus</a> (<code>+</code>)</td>
      <td>Unary operator. Attempts to convert the operand to a number, if it is not
        already.</td>
      <td>
        <p><code>+"3"</code> returns <code>3</code>.</p>

        <p><code>+true</code> returns <code>1</code>.</p>
      </td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Exponentiation">Exponentiation
          operator</a> (<code>**</code>)</td>
      <td>Calculates the <code>base</code> to the <code>exponent</code> power, that is,
        <code>base^exponent</code></td>
      <td><code>2 ** 3</code> returns <code>8</code>.<br>
        <code>10 ** -1</code> returns <code>0.1</code>.
      </td>
    </tr>
  </tbody>
</table>

<h3 id="Bitwise_operators">Bitwise operators</h3>

<p>A bitwise operator treats their operands as a set of 32 bits (zeros and ones), rather
  than as decimal, hexadecimal, or octal numbers. For example, the decimal number nine has
  a binary representation of 1001. Bitwise operators perform their operations on such
  binary representations, but they return standard JavaScript numerical values.</p>

<p>The following table summarizes JavaScript's bitwise operators.</p>

<table class="standard-table">
  <caption>Bitwise operators</caption>
  <thead>
    <tr>
      <th scope="col">Operator</th>
      <th scope="col">Usage</th>
      <th scope="col">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_AND">Bitwise
          AND</a></td>
      <td><code>a &amp; b</code></td>
      <td>Returns a one in each bit position for which the corresponding bits of both
        operands are ones.</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_OR">Bitwise
          OR</a></td>
      <td><code>a | b</code></td>
      <td>Returns a zero in each bit position for which the corresponding bits of both
        operands are zeros.</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_XOR">Bitwise
          XOR</a></td>
      <td><code>a ^ b</code></td>
      <td>Returns a zero in each bit position for which the corresponding bits are the
        same.<br>
        [Returns a one in each bit position for which the corresponding bits are
        different.]</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_NOT">Bitwise
          NOT</a></td>
      <td><code>~ a</code></td>
      <td>Inverts the bits of its operand.</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Left_shift">Left
          shift</a></td>
      <td><code>a &lt;&lt; b</code></td>
      <td>Shifts <code>a</code> in binary representation <code>b</code> bits to the left,
        shifting in zeros from the right.</td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Right_shift">Sign-propagating
          right shift</a></td>
      <td><code>a &gt;&gt; b</code></td>
      <td>Shifts <code>a</code> in binary representation <code>b</code> bits to the right,
        discarding bits shifted off.</td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Unsigned_right_shift">Zero-fill
          right shift</a></td>
      <td><code>a &gt;&gt;&gt; b</code></td>
      <td>Shifts <code>a</code> in binary representation <code>b</code> bits to the right,
        discarding bits shifted off, and shifting in zeros from the left.</td>
    </tr>
  </tbody>
</table>

<h4 id="Bitwise_Logical_Operators">Bitwise logical operators</h4>

<p>Conceptually, the bitwise logical operators work as follows:</p>

<ul>
  <li>The operands are converted to thirty-two-bit integers and expressed by a series of
    bits (zeros and ones). Numbers with more than 32 bits get their most significant bits
    discarded. For example, the following integer with more than 32 bits will be converted
    to a 32 bit integer:
    <pre>Before: 1110 0110 1111 1010 0000 0000 0000 0110 0000 0000 0001
After:               1010 0000 0000 0000 0110 0000 0000 0001</pre>
  </li>
  <li>Each bit in the first operand is paired with the corresponding bit in the second
    operand: first bit to first bit, second bit to second bit, and so on.</li>
  <li>The operator is applied to each pair of bits, and the result is constructed bitwise.
  </li>
</ul>

<p>For example, the binary representation of nine is 1001, and the binary representation
  of fifteen is 1111. So, when the bitwise operators are applied to these values, the
  results are as follows:</p>

<table class="standard-table">
  <caption>Bitwise operator examples</caption>
  <thead>
    <tr>
      <th scope="col">Expression</th>
      <th scope="col">Result</th>
      <th scope="col">Binary Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>15 &amp; 9</code></td>
      <td><code>9</code></td>
      <td><code>1111 &amp; 1001 = 1001</code></td>
    </tr>
    <tr>
      <td><code>15 | 9</code></td>
      <td><code>15</code></td>
      <td><code>1111 | 1001 = 1111</code></td>
    </tr>
    <tr>
      <td><code>15 ^ 9</code></td>
      <td><code>6</code></td>
      <td><code>1111 ^ 1001 = 0110</code></td>
    </tr>
    <tr>
      <td><code>~15</code></td>
      <td><code>-16</code></td>
      <td><code>~ 0000 0000 ... 0000 1111 = 1111 1111 ... 1111 0000</code></td>
    </tr>
    <tr>
      <td><code>~9</code></td>
      <td><code>-10</code></td>
      <td><code>~ 0000 0000 ... 0000 1001 = 1111 1111 ... 1111 0110</code></td>
    </tr>
  </tbody>
</table>

<p>Note that all 32 bits are inverted using the Bitwise NOT operator, and that values with
  the most significant (left-most) bit set to 1 represent negative numbers
  (two's-complement representation). <code>~x</code> evaluates to the same value that
  <code>-x - 1</code> evaluates to.</p>

<h4 id="Bitwise_Shift_Operators">Bitwise shift operators</h4>

<p>The bitwise shift operators take two operands: the first is a quantity to be shifted,
  and the second specifies the number of bit positions by which the first operand is to be
  shifted. The direction of the shift operation is controlled by the operator used.</p>

<p>Shift operators convert their operands to thirty-two-bit integers and return a result
  of either type {{jsxref("Number")}} or {{jsxref("BigInt")}}: specifically, if the type
  of the left operand is {{jsxref("BigInt")}}, they return {{jsxref("BigInt")}};
  otherwise, they return {{jsxref("Number")}}.</p>

<p>The shift operators are listed in the following table.</p>

<table class="fullwidth-table">
  <caption>Bitwise shift operators</caption>
  <thead>
    <tr>
      <th scope="col">Operator</th>
      <th scope="col">Description</th>
      <th scope="col">Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Left_shift">Left
          shift</a><br>
        (<code>&lt;&lt;</code>)</td>
      <td>This operator shifts the first operand the specified number of bits to the left.
        Excess bits shifted off to the left are discarded. Zero bits are shifted in from
        the right.</td>
      <td><code>9&lt;&lt;2</code> yields 36, because 1001 shifted 2 bits to the left
        becomes 100100, which is 36.</td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Right_shift">Sign-propagating
          right shift</a> (<code>&gt;&gt;</code>)</td>
      <td>This operator shifts the first operand the specified number of bits to the
        right. Excess bits shifted off to the right are discarded. Copies of the leftmost
        bit are shifted in from the left.</td>
      <td><code>9&gt;&gt;2</code> yields 2, because 1001 shifted 2 bits to the right
        becomes 10, which is 2. Likewise, <code>-9&gt;&gt;2</code> yields -3, because the
        sign is preserved.</td>
    </tr>
    <tr>
      <td><a
          href="/en-US/docs/Web/JavaScript/Reference/Operators/Unsigned_right_shift">Zero-fill
          right shift</a> (<code>&gt;&gt;&gt;</code>)</td>
      <td>This operator shifts the first operand the specified number of bits to the
        right. Excess bits shifted off to the right are discarded. Zero bits are shifted
        in from the left.</td>
      <td><code>19&gt;&gt;&gt;2</code> yields 4, because 10011 shifted 2 bits to the right
        becomes 100, which is 4. For non-negative numbers, zero-fill right shift and
        sign-propagating right shift yield the same result.</td>
    </tr>
  </tbody>
</table>

<h3 id="Logical_operators">Logical operators</h3>

<p>Logical operators are typically used with Boolean (logical) values; when they are, they
  return a Boolean value. However, the <code>&amp;&amp;</code> and <code>||</code>
  operators actually return the value of one of the specified operands, so if these
  operators are used with non-Boolean values, they may return a non-Boolean value. The
  logical operators are described in the following table.</p>

<table class="fullwidth-table">
  <caption>Logical operators</caption>
  <thead>
    <tr>
      <th scope="col">Operator</th>
      <th scope="col">Usage</th>
      <th scope="col">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND">Logical
          AND</a> (<code>&amp;&amp;</code>)</td>
      <td><code>expr1 &amp;&amp; expr2</code></td>
      <td>Returns <code>expr1</code> if it can be converted to <code>false</code>;
        otherwise, returns <code>expr2</code>. Thus, when used with Boolean values,
        <code>&amp;&amp;</code> returns <code>true</code> if both operands are true;
        otherwise, returns <code>false</code>.</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Logical_OR">Logical OR
        </a>(<code>||</code>)</td>
      <td><code>expr1 || expr2</code></td>
      <td>Returns <code>expr1</code> if it can be converted to <code>true</code>;
        otherwise, returns <code>expr2</code>. Thus, when used with Boolean values,
        <code>||</code> returns <code>true</code> if either operand is true; if both are
        false, returns <code>false</code>.</td>
    </tr>
    <tr>
      <td><a href="/en-US/docs/Web/JavaScript/Reference/Operators/Logical_NOT">Logical NOT
        </a>(<code>!</code>)</td>
      <td><code>!expr</code></td>
      <td>Returns <code>false</code> if its single operand that can be converted to
        <code>true</code>; otherwise, returns <code>true</code>.</td>
    </tr>
  </tbody>
</table>

<p>Examples of expressions that can be converted to <code>false</code> are those that
  evaluate to null, 0, NaN, the empty string (""), or undefined.</p>

<p>The following code shows examples of the <code>&amp;&amp;</code> (logical AND)
  operator.</p>

<pre class="brush: js">var a1 =  true &amp;&amp; true;     // t &amp;&amp; t returns true
var a2 =  true &amp;&amp; false;    // t &amp;&amp; f returns false
var a3 = false &amp;&amp; true;     // f &amp;&amp; t returns false
var a4 = false &amp;&amp; (3 == 4); // f &amp;&amp; f returns false
var a5 = 'Cat' &amp;&amp; 'Dog';    // t &amp;&amp; t returns Dog
var a6 = false &amp;&amp; 'Cat';    // f &amp;&amp; t returns false
var a7 = 'Cat' &amp;&amp; false;    // t &amp;&amp; f returns false
</pre>

<p>The following code shows examples of the || (logical OR) operator.</p>

<pre class="brush: js">var o1 =  true || true;     // t || t returns true
var o2 = false || true;     // f || t returns true
var o3 =  true || false;    // t || f returns true
var o4 = false || (3 == 4); // f || f returns false
var o5 = 'Cat' || 'Dog';    // t || t returns Cat
var o6 = false || 'Cat';    // f || t returns Cat
var o7 = 'Cat' || false;    // t || f returns Cat
</pre>

<p>The following code shows examples of the ! (logical NOT) operator.</p>

<pre class="brush: js">var n1 = !true;  // !t returns false
var n2 = !false; // !f returns true
var n3 = !'Cat'; // !t returns false
</pre>

<h4 id="Short-Circuit_Evaluation">Short-circuit evaluation</h4>

<p>As logical expressions are evaluated left to right, they are tested for possible
  "short-circuit" evaluation using the following rules:</p>

<ul>
  <li><code>false &amp;&amp; <em>anything</em></code> is short-circuit evaluated to false.
  </li>
  <li><code>true || <em>anything</em></code> is short-circuit evaluated to true.</li>
</ul>

<p>The rules of logic guarantee that these evaluations are always correct. Note that the
  <em>anything</em> part of the above expressions is not evaluated, so any side effects of
  doing so do not take effect.</p>

<p>Note that for the second case, in modern code you can use the new <a
    href="/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_operator">Nullish
    coalescing operator</a> (<code>??</code>) that works like <code>||</code>, but it only
  returns the second expression, when the first one is "<a
    href="/en-US/docs/Glossary/Nullish">nullish</a>", i.e. <a
    href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/null"
    title="The value null represents the intentional absence of any object value. It is one of JavaScript's primitive values and is treated as falsy for boolean operations."><code>null</code></a>
  or <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined"
    title="The global undefined property represents the primitive value undefined. It is one of JavaScript's primitive types."><code>undefined</code></a>.
  It is thus the better alternative to provide defaults, when values like <code>''</code>
  or <code>0</code> are valid values for the first expression, too.</p>

<h3 id="String_operators">String operators</h3>

<p>In addition to the comparison operators, which can be used on string values, the
  concatenation operator (+) concatenates two string values together, returning another
  string that is the union of the two operand strings.</p>

<p>For example,</p>

<pre
  class="brush: js">console.log('my ' + 'string'); // console logs the string "my string".</pre>

<p>The shorthand assignment operator += can also be used to concatenate strings.</p>

<p>For example,</p>

<pre class="brush: js">var mystring = 'alpha';
mystring += 'bet'; // evaluates to "alphabet" and assigns this value to mystring.</pre>

<h3 id="Conditional_ternary_operator">Conditional (ternary) operator</h3>

<p>The <a
    href="/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator">conditional
    operator</a> is the only JavaScript operator that takes three operands. The operator
  can have one of two values based on a condition. The syntax is:</p>

<pre class="brush: js"><em>condition</em> ? <em>val1</em> : <em>val2</em>
</pre>

<p>If <code>condition</code> is true, the operator has the value of <code>val1</code>.
  Otherwise it has the value of <code>val2</code>. You can use the conditional operator
  anywhere you would use a standard operator.</p>

<p>For example,</p>

<pre class="brush: js">var status = (age &gt;= 18) ? 'adult' : 'minor';
</pre>

<p>This statement assigns the value "adult" to the variable <code>status</code> if
  <code>age</code> is eighteen or more. Otherwise, it assigns the value "minor" to
  <code>status</code>.</p>

<h3 id="Comma_operator">Comma operator</h3>

<p>The <a href="/en-US/docs/Web/JavaScript/Reference/Operators/Comma_Operator">comma
    operator</a> (<code>,</code>) evaluates both of its operands and returns the value of
  the last operand. This operator is primarily used inside a <code>for</code> loop, to
  allow multiple variables to be updated each time through the loop. It is regarded bad
  style to use it elsewhere, when it is not necessary. Often two separate statements can
  and should be used instead.</p>

<p>For example, if <code>a</code> is a 2-dimensional array with 10 elements on a side, the
  following code uses the comma operator to update two variables at once. The code prints
  the values of the diagonal elements in the array:</p>

<pre class="brush: js">var x = [0,1,2,3,4,5,6,7,8,9]
var a = [x, x, x, x, x];

for (var i = 0, j = 9; i &lt;= j; i++, j--)
//                                ^
  console.log('a[' + i + '][' + j + ']= ' + a[i][j]);
</pre>

<h3 id="Unary_operators">Unary operators</h3>

<p>A unary operation is an operation with only one operand.</p>

<h4 id="delete"><code>delete</code></h4>

<p>The
  <code><a href="/en-US/docs/Web/JavaScript/Reference/Operators/delete">delete</a></code>
  operator deletes an object's property. The syntax is:</p>

<pre class="brush: js">delete object.property;
delete object[propertyKey];
delete objectName[index];
</pre>

<p>where <code>object</code> is the name of an object, <code>property</code> is an
  existing property, and <code>propertyKey</code> is a string or symbol referring to an
  existing property.</p>

<p>If the <code>delete</code> operator succeeds, it removes the property from the object.
  Trying to access it afterwards will yield <code>undefined</code>. The
  <code>delete</code> operator returns <code>true</code> if the operation is possible; it
  returns <code>false</code> if the operation is not possible.</p>

<pre class="brush: js">
delete Math.PI; // returns false (cannot delete non-configurable properties)

const myObj = {h: 4};
delete myobj.h; // returns true (can delete user-defined properties)
</pre>

<h5 id="Deleting_array_elements">Deleting array elements</h5>

<p>Since arrays are just objects, it's technically possible to <code>delete</code>
  elements from them. This is however regarded as a bad practice, try to avoid it. When
  you delete an array property, the array length is not affected and other elements are
  not re-indexed. To achieve that behavior, it is much better to just overwrite the
  element with the value <code>undefined</code>. To actually manipulate the array, use the
  various array methods such as
  <code><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice">splice</a></code>.
</p>

<h4 id="typeof"><code>typeof</code></h4>

<p>The <a href="/en-US/docs/Web/JavaScript/Reference/Operators/typeof"><code>typeof</code>
    operator</a> is used in either of the following ways:</p>

<pre class="brush: js">typeof operand
typeof (operand)
</pre>

<p>The <code>typeof</code> operator returns a string indicating the type of the
  unevaluated operand. <code>operand</code> is the string, variable, keyword, or object
  for which the type is to be returned. The parentheses are optional.</p>

<p>Suppose you define the following variables:</p>

<pre class="brush: js">var myFun = new Function('5 + 2');
var shape = 'round';
var size = 1;
var foo = ['Apple', 'Mango', 'Orange'];
var today = new Date();
</pre>

<p>The <code>typeof</code> operator returns the following results for these variables:</p>

<pre class="brush: js">typeof myFun;       // returns "function"
typeof shape;       // returns "string"
typeof size;        // returns "number"
typeof foo;         // returns "object"
typeof today;       // returns "object"
typeof doesntExist; // returns "undefined"
</pre>

<p>For the keywords <code>true</code> and <code>null</code>, the <code>typeof</code>
  operator returns the following results:</p>

<pre class="brush: js">typeof true; // returns "boolean"
typeof null; // returns "object"
</pre>

<p>For a number or string, the <code>typeof</code> operator returns the following results:
</p>

<pre class="brush: js">typeof 62;            // returns "number"
typeof 'Hello world'; // returns "string"
</pre>

<p>For property values, the <code>typeof</code> operator returns the type of value the
  property contains:</p>

<pre class="brush: js">typeof document.lastModified; // returns "string"
typeof window.length;         // returns "number"
typeof Math.LN2;              // returns "number"
</pre>

<p>For methods and functions, the <code>typeof</code> operator returns results as follows:
</p>

<pre class="brush: js">typeof blur;        // returns "function"
typeof eval;        // returns "function"
typeof parseInt;    // returns "function"
typeof shape.split; // returns "function"
</pre>

<p>For predefined objects, the <code>typeof</code> operator returns results as follows:
</p>

<pre class="brush: js">typeof Date;     // returns "function"
typeof Function; // returns "function"
typeof Math;     // returns "object"
typeof Option;   // returns "function"
typeof String;   // returns "function"
</pre>

<h4 id="void"><code>void</code></h4>

<p>The <a href="/en-US/docs/Web/JavaScript/Reference/Operators/void"><code>void</code>
    operator</a> is used in either of the following ways:</p>

<pre class="brush: js">void (expression)
void expression
</pre>

<p>The <code>void</code> operator specifies an expression to be evaluated without
  returning a value. <code>expression</code> is a JavaScript expression to evaluate. The
  parentheses surrounding the expression are optional, but it is good style to use them.
</p>

<h3 id="Relational_operators">Relational operators</h3>

<p>A relational operator compares its operands and returns a Boolean value
  based on whether the comparison is true.</p>

<h4 id="in"><code>in</code></h4>

<p>The <a href="/en-US/docs/Web/JavaScript/Reference/Operators/in"><code>in</code>
    operator</a> returns <code>true</code> if the specified property is in the specified
  object. The syntax is:</p>

<pre class="brush: js">propNameOrNumber in objectName
</pre>

<p>where <code>propNameOrNumber</code> is a string, numeric, or symbol expression
  representing a property name or array index, and <code>objectName</code> is the name of
  an object.</p>

<p>The following examples show some uses of the <code>in</code> operator.</p>

<pre class="brush: js">// Arrays
var trees = ['redwood', 'bay', 'cedar', 'oak', 'maple'];
0 in trees;        // returns true
3 in trees;        // returns true
6 in trees;        // returns false
'bay' in trees;    // returns false (you must specify the index number,
                   // not the value at that index)
'length' in trees; // returns true (length is an Array property)

// built-in objects
'PI' in Math;          // returns true
var myString = new String('coral');
'length' in myString;  // returns true

// Custom objects
var mycar = { make: 'Honda', model: 'Accord', year: 1998 };
'make' in mycar;  // returns true
'model' in mycar; // returns true
</pre>

<h4 id="instanceof"><code>instanceof</code></h4>

<p>The <a
    href="/en-US/docs/Web/JavaScript/Reference/Operators/instanceof"><code>instanceof</code>
    operator</a> returns <code>true</code> if the specified object is of the specified
  object type. The syntax is:</p>

<pre class="brush: js">objectName instanceof objectType
</pre>

<p>where <code>objectName</code> is the name of the object to compare to
  <code>objectType</code>, and <code>objectType</code> is an object type, such as
  {{jsxref("Date")}} or {{jsxref("Array")}}.</p>

<p>Use <code>instanceof</code> when you need to confirm the type of an object at runtime.
  For example, when catching exceptions, you can branch to different exception-handling
  code depending on the type of exception thrown.</p>

<p>For example, the following code uses <code>instanceof</code> to determine whether
  <code>theDay</code> is a <code>Date</code> object. Because <code>theDay</code> is a
  <code>Date</code> object, the statements in the <code>if</code> statement execute.</p>

<pre class="brush: js">var theDay = new Date(1995, 12, 17);
if (theDay instanceof Date) {
  // statements to execute
}
</pre>

<h3 id="Operator_precedence">Operator precedence</h3>

<p>The <em>precedence</em> of operators determines the order they are applied when
  evaluating an expression. You can override operator precedence by using parentheses.</p>

<p>The following table describes the precedence of operators, from highest to lowest.</p>

<table class="standard-table">
  <caption>Operator precedence</caption>
  <thead>
    <tr>
      <th scope="col">Operator type</th>
      <th scope="col">Individual operators</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>member</td>
      <td><code>. []</code></td>
    </tr>
    <tr>
      <td>call / create instance</td>
      <td><code>() new</code></td>
    </tr>
    <tr>
      <td>negation/increment</td>
      <td><code>! ~ - + ++ -- typeof void delete</code></td>
    </tr>
    <tr>
      <td>multiply/divide</td>
      <td><code>* / %</code></td>
    </tr>
    <tr>
      <td>addition/subtraction</td>
      <td><code>+ -</code></td>
    </tr>
    <tr>
      <td>bitwise shift</td>
      <td><code>&lt;&lt; &gt;&gt; &gt;&gt;&gt;</code></td>
    </tr>
    <tr>
      <td>relational</td>
      <td><code>&lt; &lt;= &gt; &gt;= in instanceof</code></td>
    </tr>
    <tr>
      <td>equality</td>
      <td><code>== != === !==</code></td>
    </tr>
    <tr>
      <td>bitwise-and</td>
      <td><code>&amp;</code></td>
    </tr>
    <tr>
      <td>bitwise-xor</td>
      <td><code>^</code></td>
    </tr>
    <tr>
      <td>bitwise-or</td>
      <td><code>|</code></td>
    </tr>
    <tr>
      <td>logical-and</td>
      <td><code>&amp;&amp;</code></td>
    </tr>
    <tr>
      <td>logical-or</td>
      <td><code>||</code></td>
    </tr>
    <tr>
      <td>conditional</td>
      <td><code>?:</code></td>
    </tr>
    <tr>
      <td>assignment</td>
      <td>
        <code>= += -= *= /= %= &lt;&lt;= &gt;&gt;= &gt;&gt;&gt;= &amp;= ^= |= &amp;&amp;= ||= ??= </code>
      </td>
    </tr>
    <tr>
      <td>comma</td>
      <td><code>,</code></td>
    </tr>
  </tbody>
</table>

<p>A more detailed version of this table, complete with links to additional details about
  each operator, may be found in <a
    href="/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence#table">JavaScript
    Reference</a>.</p>

<h2 id="Expressions">Expressions</h2>

<p>An <em>expression</em> is any valid unit of code that resolves to a value.</p>

<p>Every syntactically valid expression resolves to some value but conceptually, there are
  two types of expressions: with side effects (for example: those that assign value to a
  variable) and those that in some sense evaluate and therefore resolve to a value.</p>

<p>The expression <code>x = 7</code> is an example of the first type. This expression uses
  the =<em> operator</em> to assign the value seven to the variable <code>x</code>. The
  expression itself evaluates to seven.</p>

<p>The code <code>3 + 4</code> is an example of the second expression type. This
  expression uses the + operator to add three and four together without assigning the
  result, seven, to a variable.</p>

<p>JavaScript has the following expression categories:</p>

<ul>
  <li>Arithmetic: evaluates to a number, for example 3.14159. (Generally uses <a
      href="#arithmetic_operators">arithmetic operators</a>.)</li>
  <li>String: evaluates to a character string, for example, "Fred" or "234". (Generally
    uses <a href="#string_operators">string operators</a>.)</li>
  <li>Logical: evaluates to true or false. (Often involves <a href="#logical_operators">logical
      operators</a>.)</li>
  <li>Primary expressions: Basic keywords and general expressions in JavaScript.</li>
  <li>Left-hand-side expressions: Left values are the destination of an assignment.</li>
</ul>

<h3 id="Primary_expressions">Primary expressions</h3>

<p>Basic keywords and general expressions in JavaScript.</p>

<h4 id="this"><code>this</code></h4>

<p>Use the <a href="/en-US/docs/Web/JavaScript/Reference/Operators/this"><code>this</code>
    keyword</a> to refer to the current object. In general, <code>this</code> refers to
  the calling object in a method. Use <code>this</code> either with the dot or the bracket
  notation:</p>

<pre class="brush: js">this['propertyName']
this.propertyName
</pre>

<p>Suppose a function called <code>validate</code> validates an object's
  <code>value</code> property, given the object and the high and low values:</p>

<pre class="brush: js">function validate(obj, lowval, hival) {
  if ((obj.value &lt; lowval) || (obj.value &gt; hival))
    console.log('Invalid Value!');
}
</pre>

<p>You could call <code>validate</code> in each form element's <code>onChange</code> event
  handler, using <code>this</code> to pass it to the form element, as in the following
  example:</p>

<pre class="brush: html">&lt;p&gt;Enter a number between 18 and 99:&lt;/p&gt;
&lt;input type="text" name="age" size=3 onChange="validate(this, 18, 99);"&gt;
</pre>

<h4 id="Grouping_operator">Grouping operator</h4>

<p>The grouping operator <code>( )</code> controls the precedence of evaluation in
  expressions. For example, you can override multiplication and division first, then
  addition and subtraction to evaluate addition first.</p>

<pre class="brush:js">var a = 1;
var b = 2;
var c = 3;

// default precedence
a + b * c     // 7
// evaluated by default like this
a + (b * c)   // 7

// now overriding precedence
// addition before multiplication
(a + b) * c   // 9

// which is equivalent to
a * c + b * c // 9
</pre>

<h3 id="Left-hand-side_expressions">Left-hand-side expressions</h3>

<p>Left values are the destination of an assignment.</p>

<h4 id="new"><code>new</code></h4>

<p>You can use the <a
    href="/en-US/docs/Web/JavaScript/Reference/Operators/new"><code>new</code>
    operator</a> to create an instance of a user-defined object type or of one of the
  built-in object types. Use <code>new</code> as follows:</p>

<pre class="brush: js">var objectName = new objectType([param1, param2, ..., paramN]);
</pre>

<h4 id="super">super</h4>

<p>The <a href="/en-US/docs/Web/JavaScript/Reference/Operators/super">super keyword</a> is
  used to call functions on an object's parent. It is useful with <a
    href="/en-US/docs/Web/JavaScript/Reference/Classes">classes</a> to call the parent
  constructor, for example.</p>

<pre class="brush: js">super([arguments]); // calls the parent constructor.
super.functionOnParent([arguments]);
</pre>

<div>{{PreviousNext("Web/JavaScript/Guide/Functions",
  "Web/JavaScript/Guide/Numbers_and_dates")}}</div>