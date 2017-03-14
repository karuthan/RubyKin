# 'If-Else' ஆனால் இல்லை நிபந்தனை கட்டளை 

ஒருநாள் நீங்கள் படுக்கையில் இருந்து சனிக்கிழமை எழுந்திருக்கிறீங்க: 

"அறை சுத்தம் ஆனால் நீ  விளையாட செல்லலாம், இல்லை வீட்டில் உள்ளேயே தான் இருக்க வேண்டும்" -அம்மா  

என்ற ஒரு தாளில் எழுத்தி நிபந்தனையாக அம்மா அறை கதவில் ஓட்டினாள்.

_ஆனால்_ and _இல்லை_ வாக்கியங்கள் ரூபியிடம் உங்களுக்கு என்ன திசையில் நிரல் இயக்கம் தொடரவேண்டும் என்று சொல்லியும், ரூபியின் இயக்கத்தையும் கண்காணிக்கும்.

இதுவரை, ரூபியில் எப்படி எண்களை பயன்படுத்தி கணிதம் செய்வது, சொற்களையும் வாக்கியங்களையும் சரங்களில் சேமிப்பது என்றும், இவ்விரண்டையும் மாறிலியில் கணினியின் நினைவில் சேமிப்பது என்றும் படித்து புரிந்துகொண்டோம். 
இதன் வழி நாம் கணினியில் தகவல்களை எண்களாகவும், சரம் என்றும் குறியீடு செய்ய கற்றுக்கொண்டோம் - ஆனால் இதனை வைத்து எப்படி கணினியில் இயங்கும் திசையை நிர்ணயிப்பது என்று நமக்கு இயலவில்லை.

இயங்கும் திசையை நிர்ணயிக்க ஒரு வழி நிபந்தனைகளுடன் நிரல்கள் எழுதுவது. நிபந்தனைகளுடன் இயங்கும் நிரல் என்றல் என்ன? இதனை புரிந்து கொள்ள இந்த நிலையை யோசியுங்கள்; உங்கள் பெற்றோர் உங்களை தடையில்லாமல், அளவில்லாமல்  அன்பு செலுத்துகிறார்கள் அல்லவா - அதாவது ஐம்பது சதவிகிதம் இல்லை முழு நூறு சதவிகிதம் கேள்விகள் இல்லாமல் அன்பு செலுத்துகிறார்கள் - இதனுடைய எதிர்மறையானது நிபந்தனை உடன் இருக்கும் அன்பு - "செல்லம் நீ கணக்கு பரிட்சையில் 100/100 வாங்குனால் மட்டும் உனக்கு இந்த ஆண்டு பிறந்தநாள் விழா". இந்த மட்டற்ற அன்பு, கேள்விகள் இல்லாத தூய தாயின் அன்பு கணினியிடம் கிடையாது - ரூபி இயங்குவாரத்திற்கு நிபந்தனைகளுடன் ரூபியை சமாளிக்க வேண்டும்.

சரி, நிபந்தனைகளை எப்படி பயன்படுத்துவது என்று பார்ப்போம். நிபந்தனைகளுக்கு வெளி மாறிலி நிலையை ஒட்டி தீர்வு அமையுங். உதாரணம், இங்கு  _ஏதோ ஒன்று_ நடந்தது/மாறியது, ஆனால்  _ஒரு குறிப்பிட்ட காரியம் செய்யவும்_, இல்லை, மற்றோரு  _காரியம் செய்யவும்_. உதாரணத்திற்கு: உங்களுக்கு பசித்தால், "இட்லியை சாப்பிடுங்க" , இல்லையா, "இட்லியை சாப்பிடாதீங்க"!

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
