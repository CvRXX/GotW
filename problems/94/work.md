# GotW 94

## My work 

### 1. What does this code do? 
This code takes an container and a value and adds the value tot the container if the value is not yet already in the container. I think a good name for `some function` would be `uniqueAppend`.

### 2. What does “write code against interfaces, not implementations” mean, and why is it generally beneficial?
I'm not totaly sure but I think this saying means that when writing code you should focus on meeting the pre and post conditions as declared in the interface. This is mostly benificial because it forces you to think of what the function does and not how that functionality is archieved. 

### 3. What are some popular concerns about using auto to declare variables? Are they valid? Discuss.
Using auto you don't have to write down the type of the variable you're declaring. The concerns that are often raised is that the type that a variable gets might not be known to the user. I don't think this is totaly valid. In most uses of auto it is still very clear what the type is going to be and it removes some duplicate information in your code. For example:

```
auto myCar = Car(opel);
```

It is still very clear that myCar is going to be of type Car. If we would write it without auto it wouldn't add more information:

```
Car myCar = Car(opel);
```
In my mind writing Car two times is not benficial. Another reason to use auto is for types that are really long because of templates or for types that are not named like lambda's. If auto is not used there it wouldlead to lengthy types. For lambdas it would be impossible to name them. 

### 4. When declaring a new local variable x, what advantages are there to declaring it using auto and one of the two following syntaxes:
A: 
  * The type of x can be decided on in the function.
  * If the type of x is very long it doesn't have to be written down.

B: 
  * You only have to write the type once. There is no duplicate information.

### 5. Explain how using the style suggested in #4 is consistent with, or actively leverages, the following other C++ features:
A:
Here it prevents from writing the same thing twice:
```
// Without auto:
Car myCar = new Car(opel);

// With auto:
auto myCar = new Car(opel);
```

B:
Because litteral suffixes are a way to easily define types of variables it would be redunant to also declare them instead of auto.

C: 
As discussed above because the lambda type is not know to the user without auto it would be impossible to name a lambda.

D:
For functions it would allow writing functions where the return type depends on which type it gets passed. 

E:
Not really sure what the applications are here.

### 6. Are there any cases where it is not possible to use the style in #4 to declare all local variables?
I think it would be weird and needlessly complex to write fundamental types with auto:

```
auto i = int(3);
// I think this is the better option:
int i = 3;
```

## Solution

### 1. What does this code do? What would be a good name for some_function?
I awnsered this correctly.

### 2. What does “write code against interfaces, not implementations” mean, and why is it generally beneficial?
The anwser was intressting. I like how when you look to the history of programming more and more encapsolation came into the language. I understand now that the saying means that the user should care about what the code does not how. This allows for writing more generic code and moore reusablilty.

### 3. What are some popular concerns about using auto to declare variables? Are they valid? Discuss.
I hadn't thought about lazyness. Apart from that I don't think lazyness is bad peree it's also not the reason for using auto.

It's also very cool that auto enforces you to iniate the varible. Hadn't thought of it in that way.

I like the many examples of how we don't care about types. I think I could write more generic code.

### 4. When declaring a new local variable x, what advantages are there to declaring it using auto and one of the two following syntaxes:
I did not think of accidential narrow conversions.

### 5. Explain how using the style suggested in #4 is consistent with, or actively leverages, the following other C++ features:
E:
I was thinking of a way to use auto here but the idea was to apply the right hand style by using `using`.

### 6. Are there any cases where it is not possible to use the style in #4 to declare all local variables?
- 


## What I learned.
I can use auto a lot more than I'm using it now. This will make my code more reusable and readable. 

Another thing that I learned is to care less about types. Caring about types prevents correct encapsulation.

