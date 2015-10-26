# developer-quiz

Return your answers as a zip-file. Do not fork this repo.

## Questions

Take approx. 15 minutes to answer each question. Use can use diagrams or whatever technique you find the best to explain your solution.

### Question 1.

You are implementing a service that will receive videos uploaded from a mobile client and re-encode those videos. You have thousands of clients that are uploading video at the same time. Explain the _software architecture_ for the service. What _technology/architecture/patterns_ would you use and why?

### Question 2.

How would you implement backend data storage for Facebook-messenger-like application (with similar scale), i.e. how would you store chat related data? Describe the _data model and technologies_ you would use.

### Question 3.

You are building an application running inside web browser. You have read a list of user's friends' usernames from server. List can contain thousands of usernames. You need to implement a component that finds a usernames from this list based on user input.
For example given a list of friend is `'fred', 'frank', 'jerry'`. When user types `fr`, you should filter the list so that usernames containing `fr` are included. How would you implement this i.e. _what data structures and algorithms_ would you use?

## Programming task

Implement function `diff` to find changed values in two JSON objects. You can use any programming language but no external libraries allowed (except you can add a JSON parsing library if needed) . Consider the performance of your implementation while keeping your code elegant. Provide code, tests & instructions how to run the tests. Given for example:
```
first = {
  "foo": {
    "bar": "baz",
    "biz": "foo"
  },
  "fiz": {
    "foo": "baz"
  },
  "bar": "baz",
  "baz": [
    "foo",
    "bar"
  ],
  "miss": 123
}
```
and
```
second = {
  "foo": {
    "bar": "baz1",
    "biz": "foo"
  },
  "fiz": {
    "foo": "baz"
  },
  "bar": "baz",
  "baz": [
    "foo1"
  ],
  "new_value": 1
}
```
Then `diff(first, second)` should return
```
{
  "foo": {
    "bar": "baz1"
  },
  "baz": [
    "foo1"
  ],
  "miss": "undefined",
  "new_value": 1
}
```
