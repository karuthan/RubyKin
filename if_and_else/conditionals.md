# 'If-Else' ஆனால் இல்லை நிபந்தனை கட்டளை 

ஒருநாள் நீங்கள் படுக்கையில் இருந்து சனிக்கிழமை எழுந்திருக்கிறீங்க: 

"அறை சுத்தம் ஆனால் நீ  விளையாட செல்லலாம், இல்லை வீட்டில் உள்ளேயே தான் இருக்க வேண்டும்" -அம்மா  

என்ற ஒரு தாளில் எழுத்தி நிபந்தனையாக அம்மா அறை கதவில் ஓட்டினாள்.

_If_ and _else_ statements help Ruby understand what you want her to do and when you want her to do it.

So far, we’ve learned how Ruby can perform basic math on numbers, store words and sentences as strings, and place these types of information into memory stored in variables. Now that we know how to store information and interact with it, we need a way of telling the computer what to _do_ with that information.

One way we do that is with conditionals. This is why your parents say they love you unconditionally, because there is no _if_ or _else_, there is only 100% love, no matter what. Ruby doesn’t love anything unconditionally, Ruby needs to be convinced by conditions.

A conditional is something that depends on other factors. If this _something_ happens, do _that_, otherwise, do something _else_. For example, if you are hungry, eat a sandwich, else, don’t eat a sandwich!

![Art by Vixuong Hong](http://rubykin.com/images/eat-sandwich.png)

Here’s how an If Else conditional might look in Ruby.

```ruby
# set an x variable to the value 5
x = 5

# start the if / else conditional
if x <= 10
  puts x
else
  puts "Number is greater than 10"
end
```
 
In a conditional, the computer checks to see that the code after the _if_ is true. We call this code a block, which just means a small piece of code that has some function. In this case, our block is
`X <= 10`.

So, _if_ our block is _true_ (if X is less than or equal to 10), the computer will perform the action in the next line below the if statement. Since X is equal to 5, it _is_ less than 10, and the value 5 is _put_ on the screen. If X were 11, the conditional (X <= 10) would realize this was a false statement, and the string "Number is greater than 10" would be outputted (shown) on the screen.

When the computer moves through an if-else conditional, it will follow the instructions under the _first_ if statement that evaluates to true. It then ignores all other conditions in the if-else conditional.

<br />
__What is a boolean?__

We've just learned how a conditional checks to see if something is `true` or `false`. A true or false value is called a _boolean_ in programming. We could write another conditional in a different way using booleans.

```ruby
if false
  puts "false"
elsif true
  puts "true"
else
  puts "This won’t print"
end
```

Let’s walk through each step to get a better understanding. `Nil` and `False` are the only objects in Ruby that are considered _falsy_. Something is falsy when it has a false value. `Nil` is Ruby’s way of representing nothing--nada, zip, zero! No value stored here whatsoever!

In the example above, the conditional checks to see if _false_ is true. Since the `false` object will never be true, the computer moves on to the next line to see if `true` is true. It is, so Ruby puts the string _true_ to the screen!

The final `else` will never print, because true will always evaluate to true and so the program exits before getting to the _else_ line. Remember, Ruby is only looking for the _first true_ if statement, ignoring everything else.

Here are the basic elements used to evaluate conditionals:

```ruby
<   # less than
>   # greater than
<=  # less than or equal to
>=  # greater than or equal to
==  # equal to
!=  # not equal to
```

When checking if an object is _less than_ or _greater than_, we use the same symbols found in math. When checking if some object is equal to another object, we use two equal signs. In Ruby, like many programming languages, one equal sign is used to assign or _give_ a value to a variable. If we want to check that an object is _not equal_ we use an exclamation mark before the equal sign. In Ruby, we could also simply use the word `not`.

<br />
__நிரலக்த்தில் "பொருள்" என்றால் என்ன ?__

நிரலக்த்தில் "பொருள்" என்றால் என்ன என்பதை அறிந்து கொள்ள நிஜ வாழ்க்கையில் "பொருள்" என்றால் என்ன என்பதையும் பார்த்தால் புரிந்து கொள்ள உதவியாக இருக்கும். உங்கள் விளையாட்டு பொருட்கள், செல்ல நாய்குட்டி, பந்து, கிரிக்கெட் பேட் -- இவை எல்லாமே நிஜ வாழ்க்கையில் பொருட்கள் தான். இந்த மாதிரியான நிஜ வாழ்க்கை பொருட்களின் தன்மைகளை கணினியில் குறியீடு செய்ய நம்ம பயன்படுத்த போவது நிரலாக்க "பொருள்" (Object என்று இதனை ஆங்கிலத்தில் கூறுவர்; இதுவே "object oriented programming" என்ற பொருள் நோக்கு நிரலாக்த்திர்க்கு அடிப்படையாக அமைந்த்தது.

உதாரணத்திற்கு உங்கள் தெருவில் வாழ்பவர்களின் செல்ல நாய்குட்டிகளை தினமும் நடக்க நீங்கள் கூட்டி செல்வீர்கள் என்று எடுத்து கொள்வோம். இவைகளின் பெயர்கள் : ராமு, சோமு, முத்து. 

ஒருநாள் நீங்கள் இந்த ரூபி புஷ்தகத்தை படித்துவிட்டு, "சரி இந்த நாய்குட்டிகளின் பெயரை நம்ம கணினியில் விடுவோமா?" என்று சிந்தித்தால் எப்படி இதனை சாதிப்பது ? ஏற்கெனவே படித்த "அணி" என்ற தரவமைப்பில் "சரம்" என்று மூன்று பெயர்கள் இடலாம் :

```ruby
["ராமு", "சோமு", "முத்து"]
```

மேல் உள்ள நிரல் துண்டில் மூன்று சரங்களும் பொருள் என்று ரூபிக்குள் தோற்றமளிக்கும்; அடுத்து இந்த "அணி" என்பதும் நான்காவது பொருள் என்றும் தோன்றும். ஆம் - ரூபியில் எங்கும் பொருள் உள்ளது (அணி), எதிலும் பொருள்  உள்ளது (சரம்).
<br />
<div style="text-align: center;">
__*ரூபியில் எல்லாம் பொருள் மயம்*__
</div>
<br />

இது முக்கிய பாடம் - இதுவரை புத்தகத்தில் நீங்கள் படித்த ரூபியின் அம்சங்கள் அனைத்தும் பொருள் என்று அமையும் - இவை  எண்கள், சரம், மாறிலிகள், நிபந்தனைகள், இரும தர்க்க வகைகள், ஏன் நிபந்தனை வாக்கியங்கள் கூட ...எல்லாமே "பொருள்" தான்!

அடுத்த அத்தியாயத்தில் மடக்கு (loop) வாக்கியங்கள் பற்றி கற்போம்  (அதுவும் "பொருள்" தான்!). நீங்கள் இருக்கை பிடிப்பை (seat belt) பிடித்துக்கொள்ள வேண்டாம் - இது roller coaster போன்ற வயிற்றை கலக்கும் நடுவனத்தில் மடிப்புகள் அல்ல - வெறும் மடக்கு கட்டளை தான்.

<div style="height:30px;"></div>
