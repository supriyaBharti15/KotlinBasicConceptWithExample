# KotlinBasicConceptWithExample
Fundamental concept of Kotlin | Mutable and immutable | try catch | String in Kotlin | null in Kotlin |  how to write method/function in Kotlin | create object in Kotlin
## Mutable and Immutable in Kotlin
```kotlin
# Mutable
   var name: String
   name = "supriya"
   Log.d("::TAG::", name)
   ```
   ```kotlin
# Immutable
 val roll = "123"
 Log.d("::TAG::", "roll=" + roll)
 ```
## String Templates in Kotlin
```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
        //Create object in kotlin
        var q = Question()
        
        //now print Question first
        println(q.question)
        println("Answer given by you is:=${q.answer}")
        println("Correct Answer is:=${q.correctAnswer}")
        
        //Change value of variable in class Question
        q.answer = "30"
        println("::TAG:: update Answer is ${q.answer}")
        
        //call method from class  Question
        println("::TAG:: call method from Question ${q.display()}")
    }
```
```kotlin
//this is Question Class
class Question {
        var answer = "22"
        val correctAnswer = "31"
        val question = "How many days in Jan Month?"

        fun display() {
            println("Your Correct Answer is = $correctAnswer")
        }

    }
 ```
 ## if expression 
 //compare two string using ==
 ```kotlin
        val result = if (q.answer == q.correctAnswer) {
            "Answer is correct"
        } else {
            "Answer is incorrect"
        }
        println("::TAG::  $result")
 //Output ::-- System.out: ::TAG::  Answer is correct

```

//compare using .equals() method
```kotlin
        
        val result1 = if (q.answer.equals(q.correctAnswer)) {
            "Answer Right"
        } else {
            "Answer Wrong"
        }
        println("::TAG::  $result1")
  //Output ==== System.out: ::TAG::  Answer Right
 ```
 ## null handling in Kotlin
 ```kotlin
        //create object of Question class
        //if we wants or know that any value can be null then we have to decleare value like below using ? symbol
        val q: Question? = null
        println("::TAG:: ${q?.answer} is ${q?.question}") // mendentory to check null before using object 
        //output== ::TAG:: null is null , because here null assign to object q 
 ```
## when statement in Kotlin
```kotlin

```
```kotlin
//Question Class which method we will access in main class //when statement in Kotlin
        val q = Question()
        println("::TAG::${q.printResult()}")

        //now change value of answer and see the result
        q.answer="31"
        println("::TAG::${q.printResult()}")
class Question {
        var answer = "22"
        val correctAnswer = "31"

        fun printResult() {
            when (answer) {
                correctAnswer -> println("::TAG:: u r right")
                else -> println("::TAG:: u r wrong")
            }
        }
    }
```
## for loop in Kotlin
```Kotlin
//Print number from 1 to 10
        for (k in 1..10)
            println(k) // output :- 1,2,3,4,5,6,7,8,9,10
        //print 1 to 10 and skip by 2
        for (m in 1..10 step 2)
            println(m) // Output :- 1,3,5,7,9
        //downTo :: descending order  here 10 is opening value and 7 is closing value
        for (n in 10 downTo 7 )
            println(n) // Output :- 10,9,8,7
        //Descending order with skip by 2
        for (n in 10 downTo 5 step 2)
            println(n) // Output :- 10,8,6
```
```Kotlin
//half closed range means it will print 10-1=9
        for(j in 1 until 10)
            println(j) // Output :: 1,2,3,4,5,6,7,8,9
```
```Kotlin
//list in Kotlin
        val numList = listOf(1,2,3,4,5)
        for (k in numList)
            println(k)
            
            //print elements and its index in list
        for ((index,elements) in numList.withIndex())
            println("Elements = $elements at $index")
```
```Kotlin
//TreeMap in Kotlin
        val empMap = TreeMap<String, Int>()
        //inset value in map
        empMap["emp1"] = 133
        empMap["emp2"] = 124
        empMap["emp3"] = 125
        empMap["emp4"] = 126
        empMap["emp5"] = 127
        for ((name,id) in empMap)
            println("Name ::$name ID:: $id")
```
