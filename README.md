Ecss
====

Extended CSS. Official compiler write on C. This better for integrate with Python, Ruby, Perl and compile single program.


Functional
==========

 * Comments
 * Variables
 * Operations
 * Logic
 * Macros
 * Nested
 * Functions (static)


Example
=======

Simple Ecss Code:

```
$bg_color = #222;
$fg_color = #EEE;

// Macross for pre-release crossbrowser support
border-radius($radius=0.5) {
	-webkit-border-radius: ${radius}em;
	-moz-border-radius: ${radius}em;
	border-radius: ${radius}em;
}

.header {
	color: $fg_color;
	background: $bg_color;
	border-radius();

	.logo {
		color: shade(1.5, $color);
		border-radius(0.25);

		:hover {
			color: $fg_color;
		}
	}
}
```

"compiled" to CSS:

```
.header {
	color: #EEE;
	background: #222;
	-webkit-border-radius: 0.5em;
	-moz-border-radius: 0.5em;
	border-radius: 0.5em;
}
.header .logo {
	color: #FFF;
	-webkit-border-radius: 0.25em;
	-moz-border-radius: 0.25em;
	border-radius: 0.25em;
}
.header .logo:hover {
	color: #EEE;
}
```
