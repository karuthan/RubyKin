# மடக்கு வாக்கியம் (Loops)


அடிப்படையில் கணினியை பலமுறை ஒரு குறிப்பிட்ட சில கட்டளைகளை செய்ய முனைவது மடக்கு வாக்கியம். கணினி மனிதர்களை போல் இன்பம், வலி, பசி போன்ற உணர்வுகளுக்கு ஆளாகாததால் இந்த இயந்திரம் சளைக்காமல் வேலைகளை (கணக்குகளை) செய்யும் - அதற்க்கு "போர் (boredom)" அலுப்படையாமல் வேலைகளை செய்யும் திறன் கொண்டது. 

ஒரு மடக்கு வாக்கியம் (loop "லூப்" என்று ஆங்கிலத்தில் சொல்வார்கள்) என்பது ஒரே செயலை (அல்லது சில குறிப்பிட்ட செயல்களை) பலமுறை திரும்ப திரும்ப செய்யும் பொருள் கொண்டது; கணினி ஒரு மின் இயந்திரம் என்பதால் கடகட என்று நொடிக்கு பல மில்லியன் "flops" (floating-point operations per second) என்ற வேகத்தில் நீங்கள் இட்ட மடக்கு வாக்கியம் சூழ்ந்த கட்டளைகளை கண்சிமிட்டும் நேரத்தில் இயக்கி முடிக்கும். கீழ் வரும் நிரல் துண்டை படித்து அதில் உள்ள "while" மடக்கு வாக்கியத்தை ஆராய்ந்து பார்க்கலாம் வாருங்கள்.

```ruby
x = 0
while x < 5
  puts x
  x = x + 1
end
puts "மடக்கு கட்டளை முடிந்தது"
```

 மடக்கு வாக்கியத்த ரூபி மொழியில் இந்த எடுத்துக்காட்டு விளக்கியது.  _while_ என்ற குறிச்சொல் அடுத்து வரும் மாறி 'true' (உண்மை) என்றவரை மட்டுமே இந்த மடக்கு வாக்கியம் தொடர்ந்து இயங்கும் -  இங்கு அது 
 x என்ற மாறியின் மதிப்பு 5 ஆகும் வரை இயங்கும். அதன் பின் மடக்கு கட்டளைகளில் இருந்து வெளியேறி 
 "மடக்கு கட்டளை முடிந்தது" என்ற செய்தியை அச்சிட்டு முடியும்.

மேல் கொடுக்கப்பட்ட மடக்கு வாக்கியம் ஒரு நிபந்தனை  
(x < 5)
உண்மையாக இருக்கும் வரை அதனுள் உள்ள எல்லா கட்டளைகளையும் இயக்கும்.உங்கள் பெற்றோர் நீங்க சாலையை தாண்டும் வரை இரண்டு பக்கமும் கவனம் செலுத்த சொல்வாங்க இல்லையா ? அதே போல தான் இந்த வரை எனும் _while_ கட்டளை செயல்படும். அதாவது உங்கள் பெற்றோர்கள் உங்களையே நிரல்படுத்துகிறது 
போல என்றும் சொல்லலாம் - அதாவது சாலையில் இரண்டு பக்கமும் கார்கள் இல்லாத வரை மட்டுமே நீங்கள் சாலையை கடக்கலாம்.

ரூபி கட்டளை  `puts` திரையில் அதனை சார்ந்த மதிப்பை அச்சிடும்; கொஞ்சம் நுட்பமாக சொல்லவேண்டுமானால் திரையில் அச்சிட 
`puts` என்ற கட்டளைக்கு ஒத்து வரும் மதிப்பை எடுத்துக்கொள்ளும் - அடுத்து இந்த மதிப்பு திரையில் அச்சாகும்!

கீழ் கண்ட மாதிரி கட்டளைகள் (pseudocode) என்பது _while_ மடக்கு வாக்கியம் எப்படி செயலாற்றும் என்று விளக்கும் வண்ணம் கொடுக்கப்பட்டது
```
# pseudo code
1) x is 0
2) Is 0 less than 5? True. puts x. x = 0 + 1. x is 1.
3) Is 1 less than 5? True. puts x. x = 1 + 1. x is 2.
4) Is 2 less than 5? True. puts x. x = 2 + 1. x is 3.
5) Is 3 less than 5? True. puts x. x = 3 + 1. x is 4.
6) Is 4 less than 5? True. puts x. x = 4 + 1. x is 5.
7) Is 5 less than 5? False. Loop ends.
8) "while மடக்கு வாக்கியம் முடிந்தது." is printed to the screen.
```

In this example, the x variable is set to zero outside the while loop. When the while loop begins, the computer checks to see if x is less than 5. Since 0 is less than 5, this is a true statement and the computer moves on to puts x, which displays the value of x to the screen. The next operation is to assign x the value of x + 1 (in this case 0 + 1). When it gets to the end, the loop repeats to see if x is still less than 5. Since 1 is less than 5, we put 1 to the screen and assign x the value of 1 + 1, and the process continues. Once x is equal to 5, the loop stops because the statement (5 < 5) is no longer true, it's false. After exiting the loop the computer executes the final puts statement.

The end result looks something like this:

```
0
1
2
3
4
while மடக்கு வாக்கியம் முடிந்தது.
```

![Art by Vixuong Hong](http://rubykin.com/images/roller-coaster.png)

<br />
_While_ loops are great for counting, but they can be used in other ways as well. For example, what if we played a game that wouldn’t let the player move forward unless they got the right answer?

```ruby
answer = ""  #காலி சரம் ஒன்றை உருவாக்குங்கள் 
while answer != "Ruby"
  puts "மன்னிக்கவும் தவரான விடை." unless answer == ""
  puts "மிக சிறந்த கணினி மொழி எது?"
  answer = gets.chomp
end
puts "அடி சக்கை!"
```

We are using a few new Ruby vocab words, or methods: `gets` and `chomp`. Don't worry, we will get to methods later, but here's what's happening.

In the example above, the computer will continue to prompt the user for "the best programming language" until the answer equals "Ruby". We assign the users answer to the variable `answer` using the built-in Ruby method `gets`. Gets is like a little helper monkey that helps the computer "get" a piece of information that is entered into the terminal.

Chomp is also a method. Its special task is to remove the last _new line_ character. When you hit _enter_ the `\n` new line character get stored, but chomp will remove it.

Gets and chomp are merely methods we use to cleanly assign the user’s input to the answer variable (without that strange new line character). Once the user enters the right answer, the computer exits the loop and ‘That’s right!’ is printed to the screen.


We can look at another example using a _for loop_.

```ruby
for number in 1..5 do
  puts "தற்போதைய மதிப்பு #{number}"
end
```

The for loop starts without a true condition being met. This loop will execute the code block between _do_ and _end_ once for every number in the range 1 through 5 (that's the 1..5 part). The word `number` is just a temporary variable that represents each item within our _for loop_ range. For example, a range of 2 through 8 would be written 2..8. A range of 1 through 25 would be written 1..25. Easy, right?

The funny number sign and curly brackets is a string interpolation. We will cover this later, but all you need to know right now is that it places the value of our _number_ variable inside the string. The output would look like this:

```
தற்போதைய மதிப்பு 1
தற்போதைய மதிப்பு 2
தற்போதைய மதிப்பு 3
தற்போதைய மதிப்பு 4
தற்போதைய மதிப்பு 5
```

Hopefully you are beginning to see the power of loops in Ruby. There are a few other loops, but _while_ and _for_ are the standard ones to start with. When we combine loops with collections, our programs become even more valuable!

Imagine a comic book collection, or a marble collection, or a toy collection. They are full of individual comics or marbles or toys. Imagine how much easier it would be to count, sort and organize our collections if we had the super fast computers helping us while we do other things! Next, we’ll show you how to get Ruby's help in handling collections. For now we'll finish the chapter with some examples.

<div style="height:30px;"></div>
