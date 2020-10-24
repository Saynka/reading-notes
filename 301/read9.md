# FUNCTIONAL PROGRAMMING

https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa

## What is functional programming?

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

## Pure functions

Here is a very strict definition of purity:

* It returns the same result if given the same arguments (it is also referred as deterministic)

* It does not cause any observable side effects

It returns the same result if given the same arguments
Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius * PI:

## Not Pure functions

* Reading Files
If our function reads external files, it’s not a pure function — the file’s contents can change.

* Random number generation
Any function that relies on a random number generator cannot be pure.

* It does not cause any observable side effects
Examples of observable side effects include modifying a global object or a parameter passed by reference.
Now we want to implement a function to receive an integer value and return the value increased by 1.

## Pure functions benefits

The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:
* Given a parameter A → expect the function to return value B
* Given a parameter C → expect the function to return value D
A simple example would be a function to receive a collection of numbers and expect it to increment each element of this collection.

## SLUGIFY

class UrlSlugify
  attr_reader :text
  
  def initialize(text)
    @text = text
  end

  def slugify!
    text.downcase!
    text.strip!
    text.gsub!(' ', '-')
  end
end

UrlSlugify.new(' I will be a url slug   ').slugify! # "i-will-be-a-url-slug"

## map
Map
The idea of map is to transform a collection.
The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.
Let’s get the same people collection above. We don't want to filter by “over age” now. We just want a list of strings, something like TK is 26 years old. So the final string might be :name is :age years old where :name and :age are attributes from each element in the people collection.

## JavaScript refactor example 

Scenario 1
We're an URL-shortening website, like TinyURL. We accept a long URL and return a short URL that forwards visitors to the long URL. We have two functions.
// Unrefactored code

const URLstore = [];

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  URLstore.push({[rndName]: URL});
  return rndName;
}

function getLong(shortURL) {
  for (let i = 0; i < URLstore.length; i++) {
    if (URLstore[i].hasOwnProperty(shortURL) !== false) {
      return URLstore[i][shortURL];
    }
  }
}
Problem: what happens if getLong is called with a short URL that isn't in the store? Nothing is explicitly returned so undefined will be returned. Since we're not sure how we're going to handle that, let's be explicit and throw an error so that problems can be spotted during development.

Performance-wise, be careful if you're iterating through a flat array very often, especially if it's a core piece of your program. The refactor here is to change the data-structure of URLstore.

Currently, each URL object is stored in an array. We'll visualize this as a row of buckets. When we want to convert short to long, on average we need to check half of those buckets before we find the correct short URL. What if we have thousands of buckets, and we perform this hundreds of times a second?

The answer is to use some form of hash function, which Maps and Sets use under the surface. A hash function is used to map a given key to a location in the hash table. Below, this happens when we place our short URL into the store in makeShort and when we get it back out in getLong. Depending on how you're measuring run time, the result is that on average we only need to check one bucket — no matter how many total buckets there are!
// Refactored code

const URLstore = new Map(); // Change this to a Map

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  // Place the short URL into the Map as the key with the long URL as the value
  URLstore.set(rndName, URL);
  return rndName;
}

function getLong(shortURL) {
  // Leave the function early to avoid an unnecessary else statement
  if (URLstore.has(shortURL) === false) {
    throw 'Not in URLstore!';
  }
  return URLstore.get(shortURL); // Get the long URL out of the Map
}
For those examples, we assumed that the random function wouldn't clash. 'Cloning TinyURL' is a common system design question and a very interesting one at that. What if the random function does clash? It's easy to tack on addendums about scaling and redundancy.

