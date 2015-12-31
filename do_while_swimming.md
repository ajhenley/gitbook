The while loop is good when you don't know how many times a block of code or statement should repeat and you want to continue as long as some condition it true. It looks like this:
```java
while (expression) {
 // do you thing as long as the expression is true
}
```
The while loop will never run if the expression isn't true. So if you're reading from a file while the file is open and the file isn't open then the loop won't run. So there are lots of times when the while loop may not even run.
```java
bool run = false;
while (run){
    //this code would never run
}
```

The do-while loop is similar to the while loop except the expression isn't evaluated until the loop has run at least once.
```java
bool run = false;
do {
    //this code would run once but that's it.
}while (run);
```


