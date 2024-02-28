In [[javascript]] the [[ternary operator  (?)]] is used for boolean operations. Its syntax is different from what one is normally used to seeing because it involves three variables.

The exact syntax is seen below. 
```
condition ? value_if_true : value_if_false
```

A more concrete example would be:
```
ignored ? 1 : 0
```
Here, it does not provide a lot of context, but that is normal because the ternary operator is mostly used within a larger scope, and not by itself.

one example that provides a little more context is to use it in a return statement:
```
funtion checkMembership(person){
	return person.isMember ? "yes" : "no"
} 
```

It might have occured by you that the functionality of a ternary operator can be achieved with an if-else statement, and that is correct. In fact the ternary operator is little more that short hand notation for and if-else pair. 

e.g.:
```
function checkMembership(person){
	if (person.isMember) {
		return "yes"
	}
	else {
		return "no"
	}
}
```
is the exact same function as the one using the ternary operator, but you could imagine that the notation using the ternary operator is more clean to an experienced eye and also requires less lines. All in all it is a better code practice, because of its cleanliness. 