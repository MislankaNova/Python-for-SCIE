#   Python Course in Preparation for A-Level Computing #
*for computing students who wishes to learn some programming skill fast*

*please notice that this tutorial talks about python 2, rather than python 3*

##  General Advice

1. If you find it hard to understand something, try to write some code by yourself and see how your program will work.
2. Try to write simple programs for yourself, by doing so you are receiving precious programming experience.
3. When you encounter any problem or don't know how to do a certain thing, look for solution online, there are plenty of resources, experiences, tutorials and even codes on your disposal.

##  Introduction to Python ##
### Get Python ###

If you are using OS X, your system should have Python already.

If you are using Windows, go to [www.python.org](https://www.python.org/) and download Python 2. Simply install the package and you will have Python running on your computer.

### Basic Concepts of Python ###
Python is an interpreted language, this means that when a python program is ran, lines of code are executed one by one. For example, say you have the following code:
    
    print 'Hello.'
    print 'Nice to meet you.'
    print 'Python.'


It's obvious that first you will see 'Hello.', then 'Nice to see you.' and after that 'Python.', like this:

> Hello.
> 
> Nice to meet you.
> 
> Python.

Each line in the program is called a **statement**, a statement is an instruction given to the computer to let it perform some action. In the previous example, the statement 'print 'Hello.'' makes the computer print out 'Hello.'. 

*Remember the use of 'print', as we will be using it throughout the learning of Python.*

There are two cases where a line is not executed. If your code contains an error, the program will not be able to execute the statement with such an error and quit.

    print 'Hello.'
    primt 'Nice to meet you.'
    print 'Python.'

The second line contains a typo. You will only receive 'Hello.', but not 'Nice to meet you.' nor 'Python.'

*If your program is forced to shut because of an error, you will receive a message telling you where the error is.*

Another case is when you have **comment** in your code. A comment is something in the code that is ignored by the computer, whatever in the comment is simply not executed. In python, text after a '#' is a comment and will not be executed. 

    print 'Hello.' # Hello!
    #print 'Nice to meet you.'
    print 'Python.' # Python is good

> Hello.
> 
> Python.

The second line of code is ignored, the meaningless things at the end of the other two lines are ignored as well.

*When writing your code, pay attention to comments. In your exam you need to use comments to show your examiner the meaning of your code and what your variables stand for. When you are working with others you will need to write good comments as well, otherwise it would be hard for others to understand your code.*

You may know that Python comes with two modes. In the interpreter mode, you may type in a line of code and press enter to have it ran, while you can also write the whole program down first and run all the code at once. In this tutorial we will be only discussing the second way of running Python, since this is what you have to do during your exam and when doing actual works.

### Python 2 vs. Python 3

There are two versions of Python that is currently widely used. The older one is Python 2, while Python 3 is the latest version. Although the general syntax rule is the same, there are some major differences like:

- In Python 2, you write ```print 'hello'```, while in Python 3 you should use ```print('hello')```.
- ```range``` gives different results in Python 2 and Python 3.
- ```input``` works in different ways in Python 2 and Python 3. *This is an important difference, there will be a a section in this tutorial talking about ```input``` later.*

In this tutorial, we will only learn Python 2. The reason is that there is a possibility that the examiners may be unfamiliar with the new version of Python. To let the examiners know the version you are using in the exam, please write the following in the beginning of your program code written in the exam:

    # Using Python 2

##  Basic Arithmetic ##
### ```print``` ###

As we have demonstrated before, you can use 'print' to display a line of text. A common myth is that most programmers start programming by writing the following program, but programmers are intelligent human beings, why not try something unique?

    print 'hello, world'

After executing this, you may see the following on your screen:

> hello, world

As you see, the text you want to display is contained in quotation marks. Text placed in quotation marks in Python is a **string**, which we will discuss very, very soon in...

### Data Types ###

You may have learned the concept of **data types** in CS already. Here we will just talk about some basic data types in Python.

#### Integer####

An **integer** is simply a whole number, like ```1```, ```2```, ```42```, ```999```, ```-1024``` and so on. In Python, the following are all integers:

    1
    2
    42
    -1

#### Float####

**Float** numbers are basically numbers with decimal points, like ```3.14```, ```2.54```, ```10.24```, ```2.0``` and so on. Here are some examples in Python:

    3.14
    0.1
    -0.1
    1.0

Notice that float numbers are not 100% accurate, due to the way the number is represented. In Python a well-known phenomenon is that 0.1 + 0.1 + 0.1 gives something other than 0.3. This inaccuracy is however not going to affect your program unless you require extreme accuracy.

#### String####

A **String** is a section of text, enclosed by a pair of quotation marks. You may have short strings like ```'OK'```, or longer ones like ```'In the world's end they are haunted, killed, degenerated, abandoned, dominated.'```, or digits like ```'12345'```. The following are all valid strings in Python:

    'Hello'
    "Style of quotation doesn't matter in Python"
    'A'
    "3.14159265"

Notice that the last one is not a float, it's a string, since the number is enclosed by quotation marks, making it a string rather than a float. Both double and single quotation marks are accepted, as long as the two quotation marks containing the string match. The following string will not work:

    "A BAD BAD STRING'

#### Boolean####

**Boolean** means true or false, there are only two possible values for Boolean, which are...

    True
    False

### Variables ###

In mathematics people frequently use characters to represent values. You may use x to represent something and y to represent something else. The same can be done in Python. Say you have the following program:

    print 'I love eating Ramen.'

This is perfectly working. But what if we try to represent the string using a letter x?

    x = 'I love eating Ramen.'
    print x

In the code above, the equation mark **assigns** the value 'I love eating Ramen.' to the variable, x, so x can be used in same ways 'I love eating Ramen.'. Both programs would display the following line:

> I love eating Ramen.

Of course, after assigning a value to a variable, we can change its value later, as demonstrated in the following code:

    number = 3
    print number
    number = 4
    print number

Which will show the following lines on the screen:

> 3
> 
> 4

*Please give proper names to variables when you are coding. A variable named ```number_of_people``` is easier for others to understand compared ```nop```.*

Now, you may try to answer this question: when you wish to print the word 'number', why do you have to write ```print 'number'```, putting a pair of quotation marks around the six letters, rather than just writing ```print number```?

The answer would not be hard to figure out after knowing the concept of variables.

When you write ```print number```, the program looks for a variable which is called ```number```, and then tries to ```print``` the value the variable represents. For example, if you have previously put down ```number = 10```, then the number '10' will be printed out. Alternatively, if you have never assigned a value to ```number```, then the program will crash because there is no variable named 'number'.

In contrast, if you write ```print 'number'``` in your code, the program will simply print out the text enclosed by the pair of quotation marks. You may also try things like ```print 100``` or ```print 3.14```, which will simply print out the numbers.

*Keep in mind that name of variables cannot start with a digit.*

### Calculations ###

Calculations can be carried out in Python in a very simple way. You may first try out the following program:

    x = 10
    y = x + 10
    sum = x + y
    print x
    print y
    print sum

The outcome would be too easy for us to know:

> 10
>  
> 20
>  
> 30

Of course, multiplications and divisions can be done easily as well:

    height = 2.5
    width = 0.5
    length = 1.2
    mass = 12
    volume = height * width * length
    density = mass / volume
    print volume
    print density

The volume and density will then be printed:

> 1.5
>
> 8.0

Brackets can be used as well, to allow some calculation to be carried out first.

    test_1 = 90
    test_2 = 95
    test_average = (test_1 + test_2) / 2
    print test_average

The above code prints:

> 92

The reason why ```92``` is printed instead of the actual answer ```92.5``` will be explained in next chapter.

*If you have no idea in what order the calculation will be carried out, feel free to add brackets to clarify the sequence.* 

You can also use ```**``` to give an exponent to a number.

    print 2**10

Gives:

> 1024

*Spaces between numbers and mathematical operators are not necessary, however your program code will be easier to read with these spaces.*

There are two ways to add or subtract the value of a variable:

    number = 100
    print number
    number = number + 1
    print number
    number += 1
    print number
    number = number - 10
    print number
    number -= 10
    print number

Executing the above code gives:

> 100
>
> 101
>
> 102
>
> 92
>
> 82

You may also find the reminder of a division using ```%``` and the integer part of the quotient using ```//```.

    print 10 % 3
    print 10 // 3

The result will be:

> 1
>
> 3

### Comparing Numbers ###

In Python, you may also use ```>```, ```<```, and ```==``` to compare two values. Notice that the last one is two equation marks put together (```==```), while a single equivalent mark (```=```) is used to assign a value to a variable, which is different.

When you do calculations, you get the result as numbers. However, when you compare two values, you get the result as Boolean values, that is, ```True``` or ```False```. Here we have an example:

    print 1 == 1
    print 100 > -100
    print 10 == 20
    print 0 < -1

You will get:

> True
>
> True
>
> False
>
> False

Another two symbols, ```<=``` and ```>=```, can also be used in a very obvious way.

    print 10 >= 10
    print 20 <= 10

The code gives:

> True
> 
> False

### A Word on Division ###

Read the following code:

    print 10/3
    print 8/5

At a first glance, you may except of the following results to be given:

> 3.33333333333
>
> 1.6

However, what Python will give you actually is:

> 3
>
> 1

You are dividing an integer by another integer that is not a factor of it, in mathematics, you should get a decimal number, however, Python disagrees, why?

Now, try this code below:

    print 10.0 / 3
    print 8 / 5.0

You will get:

> 3.3333333333333335
>
> 1.6

This does make more sense. If you look at the code above, you may notice the difference that there are decimal points added to one of the numbers involved in the division, however, mathematically, the numbers are not different.

So, where is the difference?

The answer is, in Python, numbers like ```10``` and ```8``` are integers, and ```10.0``` and ```8.0``` are floats, which contain decimal points. When you divide an integer by another integer in Python, the outcome would always be an integer as well. If you want to get the mathematically correct outcome, you can change any of the two numbers, or both, into floats, by adding a decimal point. Any calculation involving floats gives outcome as a float, your result will make more sense.

### A Word on Floats ###

You may have noticed that in the previous section, when you do this in Python:

    print 10.0/3

You get this result:

> 3.3333333333333335

Which is not perfectly accurate, as you would except nothing but a series of threes.

Such an error is caused by the nature of float numbers. The way in which a float number is stored in a computer makes it unable to represent a decimal number at 100% accuracy. In Python, you may even have the following:

    print 0.1 + 0.1 + 0.1 == 3

Which gives:

> False

There are ways to overcome this problem, making calculations involving decimal numbers perfectly accurate. However, in most mundane cases, the error is so small that it can be neglected without causing big problems, and you may just use normal floats in your program.

### Operations on Strings ###

In Python, strings can be added together as well, as demonstrated in the following code

    first = 'Pyt'
    second = 'hon'
    full = first + second
    print full

As you would except, you should have this:

> Python

The second string is attached to the end of the first string. Notice that there is no way to 'subtract' something from a string. In the future, we will discuss more ways to manipulate strings using the concept of lists.

Alternatively, you can also do the following:

    first = 'Pyt'
    second = 'hon'
    print first, second

Which will give:

> Pyt hon

You may ```print``` out a number of things at the same time just like in the example above. Numbers, Booleans and other things can be printed out in the same manner:

    number1 = 20
    number2 = 30
    comapre = number1 > number2
    print 'Is', number1, 'greater than', number2, '?', compare

You will get this result:

> Is 20 greater than 30 ? False

*Keep in mind that any text enclosed in quotation marks are strings and anything else is not.*

### Inputting Numbers ###

Up until now, we have been giving values to variables in the code. However, in a real program, you may need to let the user to input a value. In Python 2, this can be done using ```input()``` and ```raw_input()```. The following code demonstrate how you can achieve this.

*Notice that this doesn't apply to Python 3!*

    print 'Please type in a number and press Enter.'
    number = input()
    squared = number * number
    print number, 'times', number, 'is', squared

When this program is ran, you will first see only one line displayed:

> Please type in a number and press Enter.

You will then need to write down a number and then press Enter. Say you wan to see 10 squared:

> Please type in a number and press Enter.
> 
> 10
> 
> 10 times 10 is 100

In the above code, ```input()``` is a function which returns a value. The value given is then assigned to ```number```, that is, ```number``` will now equal whatever number you have inputted.

In this example, if you input 10, what actually happened is:

    number = 10

*Try other numbers and other uses of ```input``` as well.*

### Inputting Strings ###

If you try to use ```input()``` to let the user enter a string.

    name = input()
    print 'hello', name

Say you are Alice, you may expect this to happen.

> Alice
>
> hello Alice

However, what you actually get is an error:

>Alice
>
>Traceback (most recent call last):
>
>  File "<pyshell#2>", line 1, in <module>
>  
>    name = input()
>    
>  File "<string>", line 1, in <module>>
>  
>NameError: name 'Alice' is not defined

The error is caused by the fact that when you inputted 'Alice', Python tried to look for a variable named ```Alice```, and assign the value of ```Alice``` to ```name```. Since ```Alice``` doesn't  exist, the program runs into an error and crashes.

To overcome this problem, we may use ```raw_input()``` instead of ```input()```. The following is a working example:

    name = raw_input()
    print 'hello', name

Which will show the following to someone named Alice:

> Alice
> 
> hello Alice

What ```raw_input()``` does is that it gives a value that is a string. So, in the example above, you are actually assigning the value ```'Alice'``` to ```name```, which is the same as the following code:

    name = 'Alice'

When you are using ```raw_input()```, even if you input numbers, it will be treated as strings, for example, say you have:

    digits = raw_input()

If you put down 65536, what actually happened is:

    digits = '65536'

But not:

    digits = 65536

*To sum up, when you are asking the user to input a **number**, use ```input()```. If you want them to input a string, use ```raw_input()```.*

### Converting Data Type ###

An intelligent bandit leader is going to share some money he robbed from someone using the following code:

    print 'We are going to decide how are we going to share the money.'
    print 'Please input the number of people.'
    number = input()
    print 'Please input the amount of money.'
    money = input()
    each = money / number
    print 'Each person will receive:', each

Say there are five people and there are 128 RMB, than the following will happen:

> We are going to decide how are we going to share the money.
> 
> Please input the number of people.
> 
> 5
> 
> Please input the amount of money.
> 
> 128
> 
> Each person will receive: 25

As we had talked about before, in Python, when an integer is divided by an integer, the result will be an integer as well. This is not we want to have. To get a accurate result in decimal, we have to make one of the two numbers a float, so the result will be a float as well.

To turn a integer into a float, we use ```float()``` in the following manner:

    money = input()
    money = float(money)
    each = money / number

By using ```float()```, money is turned into a float number, so when carrying out ```each = money / number```, since ```money``` is a float (```128.0``` in this case), the result will be a float as well, the result will be accurate.

> Each person will receive: 25.6

There are different conversions that can be made.

- ```int()``` converts things into integer.
- ```float()``` converts things into float.
- ```str()``` converts things into string.

We had learned the way in which we can join two strings:

    string1 = 'str'
    string2 = 'ing'
    string3 = string1 + string2
    print string3

The above example will give:

> string

However, say we want to put one number in the end of the other number:

    number1 = 4
    number2 = 2
    number3 = number1 + number2
    print number3

What we want is '42', but what we will have is obviously:

> 6

What we can do is first turn the numbers into strings, so we will be able to join them like strings:

    number1 = 4
    number2 = 2
    number1 = str(number1)
    number2 = str(number2)
    number3 = number1 + number2
    print number3

This time, what actually happened is the same as:

    number3 = '4' + '2'

So we will get what we want:

> 42

We can even first turn integers into strings and than turn the string into integer as well:

    digit1 = 2
    digit2 = 3
    print 'The digits are:', digit1, 'and', digit2
    digit1 = str(digit1)
    digit2 = str(digit2)
    number = digit1 + digit2
    print 'The number is:', number
    number = int(number)
    number *= 2
    print 'The number times two is:', number

You will have:

> The digits are: 2, 3
> 
> The number is: 23
> 
> The number times two is: 46

*Before proceeding to the next chapter, it's strongly suggested that you try to produce a program of your own using the knowledge we have discussed in this chapter.*

##  Flow Control ##

### ```if``` ###

Say you are a teacher, who are using a Python program to produce end of semester reports for your students. With all the skills we had learned, we will not face much difficulty when writing:

    print 'Input student name'
    name = raw_input()
    print 'Input student score.'
    score = input()
    print 'The score of', name, 'is', score

This program will work fairly well. However, our ambitious teacher is not yet satisfied. He wants the program to tell if the students passed the exam or not. To achieve such a goal, we are now introducing **selection**, which is done using ```if``` in Python.

    score = input()
    if score >= 60:
        print 'PASSED'
        print 'Congratulations!'
    print 'Now carrying on to the next student.'

Here we are introducing to a lot of new stuff. Don't panic, here is a full explanation of what just happened.

```score = input()``` is fairly simple, we are now assigning a value to a variable named 'score'.

```if score >= 60:``` is where the selection takes place, please notice the column at the end of this line, which is necessary. In the previous chapter, we have talked about ways to compare numbers, here we are using these methods. In this case, if ```score``` is greater than or equal to ```60```, what will happen is...

        print 'PASSED'
        print 'Congratulations!'

These two lines may look like any other cases in which we use ```print```, however, there is one important difference. Please pay attention to the extra space before ```print```.

In programming, any space put in the beginning of a line is called **indentation**, which is especially important in Python. Indentation in Python determines whether a line of code is within a block of code or not. One level of indentation in Python should be four spaces wide.

In our example, the two lines belong to the same block of codes which are only going to be executed if ```score``` is greater than or equal to ```60```. That is, if ```socre``` is greater than or equal to 60, you will see the program say 'PASSED' and 'Congratulations!', and then 'Now carrying on to the next student.'.

However, as you would expect, if ```score``` is less then ```60```, there will be no 'PASSED' nor 'Congratulations!' displayed on the screen. However, you will still see the line 'Now carrying on to the next student.', which does not have those extra spaces at the beginning of its line.

*Try to tell the student that he is lucky when his score is ```60```.*

### ```else``` ###

Now the teacher wishes to tell the student that he didn't pass the exam, using ```else```.

    score = input()
    if score >= 60:
        print 'PASSED'
    else:
        print 'FAILED'
    print 'Now carrying on to the next student.'

What will happen is very easy to predict. If the student's ```score``` is no less than ```60```, 'PASSED' will be displayed on the screen. However, if the ```score``` is less than ```60```, 'FAILED' will display instead. You may also notice that, no matter what the score is, 'Now carrying on to the next student.' will always be displayed.

*Don't forget the column (```:```) placed at the end of the second and fourth line, this is compulsory.*

### ```elif``` ###

Say the teacher wants to let the program tell him the grade of the student, with the score provided, he therefore starts to use ```elif``` in his code:

    score = input()
    if score >= 80:
        print 'A'
    elif score >= 70:
        print 'B'
    elif score >= 60:
        print 'C'
    else:
        print 'FAILED'
    print 'Now carrying on to the next student.'

Like all previous examples, the outcome of this program is quite obvious. The computer will first check to see if ```score``` is greater than or equal to ```80```, if it is, then 'A' will be displayed and 'Now carrying on to the next student.' will be displayed. If ```score``` is less than ```80```, the program than compares it with ```70```, and then ```60``` if ```score``` is less then ```70```. Finally, if ```score``` is less than ```60```, 'FAILED' will be displayed, followed by 'Now carrying on to the next student.'.

You can use as many ```elif```s as you want in your program.

*Again, don't miss the ```:``` at the end of the lines containing ```if```, ```elif```, and ```else```.*

*Please practice your skills by using it. Can you try to write a program that will do more than this?*

### Nested ```if```s ###

Of course, you can place one ```if``` inside another. Say the students had two exams, and only those who failed both exams will fail in this subject. The teacher may write the following code:

    score1 = input()
    score2 = input()
    if score1 < 60:
        if score2 < 60:
            print 'FAILED'
        else:
            print 'PASSED'
    else:
        print 'PASSED'

In this example, the program will first check to see if ```score1``` is less than ```60```, if it is, then the student had failed in the first exam. If he had failed in the first exam, the program will then check to see if he failed in the second exam as will. If he failed both, 'FAILED' will be displayed. Otherwise, 'PASSED' will be displayed.

*Please notice the usage of indentations here. How many spaces are there at the beginning of each line?*

*If there are three exams and a student must fail all of them to eventually fail the subject, challenge yourself, write a program that will be suitable for this case.*
