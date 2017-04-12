# மாறிலி

அடிப்படையில் 'மாறிலி' (variable) என்பது கணினி நினைவகத்தில் (memory) ஒரு இடம் அனால் அதன் மதிப்பு கணினி செயலி ஓடிக்கொண்டிருக்கும் சமயம் மாறிக்கொண்டே இருக்கலாம் என்று பொருள். மாறிலி கணினியில் ஒரு மதிப்பை (data value) சேமித்துக்கொள்ளும் தன்மை உடையது. மாறிலியை உங்கள் நிரலில் பயன்செய்ய ஒரு ஆங்கில கீழ் வரிசை எழுதிதில் ஆரம்பித்து பெயரிடலாம்; அந்த மாறிலியில் மதிப்பை சேர்க்க/சேமிக்க சமன்பாடு செய்யவேண்டும்:

```
x = 12
x என்பதன் மதிப்பு என்ன ?
=> 12
```

ரூபி மொழியில் மாறிலி என்பது சமன்பாடு குறியின் இடது பக்கம் வரும் சொல். இந்த சமன்பாடு குறி (equal sign) என்பது மிக முக்கியமானது - ஏறக்குறைய எல்லா கட்டளை மொழிகளிலும் (imperative language) இதன் வலது பக்கம் வருவது மாறிலியின் மதிப்பு, இடது பக்கம் வருவது மாறிலியின் பெயர். உதாரணம் கீழே சில ரூபி மொழி மாறிலிகளை பாருங்கள்:
```ruby
myVar = "ஒரு சரம் மதிப்பு கொண்ட மாறிலி myVar"
a_long_var_name = 42
myCat = "மீசை வைத்த பூனைக்குட்டி"
```

<br />
__நினைவில் எப்படி மாறிலி சேமிக்கப்படுகின்றன ?__


கணினியில் மதிப்புகளை சேமிப்பது மின்வழி நினைவகத்தின் அமைப்பினால் சற்று தினசரி கணிதத்தை விட மாறுபட்டது. கீழ் வரும் - நாளடைவில் அது நீங்கள் நிரல்படுத்தும் அனுபவம் வருகையில் சுலபமாகும்.

கணினி மின்-நினைவகத்தை சிக்கனமாக உபயோகிக்க ஒரே தகவலை இரட்டிக்காமல் அதை நினைவு கொள்ளும். கீழ் உள்ள உதாரணங்களில்  `(அ, ஆ மற்றும் இ)` ஒரே மின்நினைவக இடத்தில், ஒரே மதிப்பை கொண்டு இருக்கும் : 12.

```
அ  = 12
ஆ  = அ
இ  = 12
```

In order to store the value 12, the computer creates a location in memory with an address, let's assume the address is ABC12. In this sense, a variable is like an X on a treasure map, guiding you to the right location.

Yet variables don't _actually_ store their information--they point to it. Or in another way, variables store memory addresses that store information. In the example above, each variable points to the same memory address that stores the number 12. This way the computer doesn't need to create three different memory locations for one value, it can use ABC12 for all three.

```
x = 12  => memory address: ABC12
y = x   => memory address: ABC12
z = 12  => memory address: ABC12
```

Now that you know how variables store information (or memory addresses) see if you can figure out the end value of X:

```
y = 5
# y points to memory address AB1,
# which contains the value 5
x = y
# x points to memory address AB1
y = 7
# y now points to memory address CD1,
# which contains 7

x equals ?
```

The trick here is to understand that X does _not equal_ Y. Remember, X only _POINTS_ to the value stored in the memory address that Y points to (AB1), at the time it was assigned. No matter what happens later to Y, the only thing X needs to remember is the location of AB1 (which will always be 5 while this program is running).

When we change the value of Y to 7, we are actually telling the computer to create a new memory address that contains the value 7 and point to it. X does not change its original address, so the value of X remains 5.

There is a built-in Ruby method called `object_id` that shows the id of the Ruby object. This can be correlated to a kind of unique memory address. Let’s look at the following example using this method.

```
y = "test" => y.object_id => 7021
x = y      => x.object_id => 7021
```

At this point, only one memory address needs to be created, since the stored value ("test") is the value for both X and Y.

```
y = "new"  => y.object_id => 8333
x equals?  => x.object_id => 7021
```

Once we change the value of Y, we create a new memory location with a new value stored (the string "new"). X does not equal "new", it still equals the value stored in the original memory address that it pointed to at the time we set X equal to Y (the string "test").

When we change variables and add new information, Ruby creates more memory locations with specific addresses--if none of the current addresses are holding the same information. And actually, Ruby has already created several object ids to help store common numbers and letters in memory, like the number 12 in our example above.

Don't worry if this is all too confusing. You don't actually _need_ to fully understand this concept to program. As we move along through the other core concepts of coding you will begin to see how variables work within the bigger picture.

The key point to remember is that an `=` equals sign in programming means "assign the value to the right of me, to the name on the left." Visually, that would look like this:

```
number12 = 12

(variable name)  (is assigned)   number 12
  number12             =               12

```

<div style="height:30px;"></div>
