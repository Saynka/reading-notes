# so basically 

html content layer
css presentatio layer
javascript behavior 

javascript and java are gonna be confusing to defferentiate at first or most likely till these become more familiar

code along

var today = new Date();
var hourNow = today.getHours();
var greetings;

if (hourNow > 18) {
    greeting = 'Good evening!';
}   else if (hourNow > 12) {
    greeting = 'Good afternoon!':
}   else if (hourNow > 0) {
    greeting = 'Good morning!':
}   else {
    greeting = 'Welcome!';
}
document.write('<h3>' + greeting + '</h3>');

