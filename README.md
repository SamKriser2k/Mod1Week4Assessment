# Mod1 Week4 Assessment
This assessment has two parts - some questions about this week's lessons, and an exercise focused on our Testing lesson. Work on the Questions first, then move on to the Exercise!

During this assessment, you may use most other resource besides your fellow students.  Feel free to google, look back at your notes, lessons, labs, etc... **you may not use Chat GPT or any other AI tool**

## Set Up

Fork this repository! (Don't clone it yet!!)

## Questions (12 Points Possible)
Edit this `README.md` file - answer the 6 questions before moving on to the exercise.  Make sure to save your changes to the README before moving on to the exercises!

To Edit the README:
* click the pencil icon in the upper right corner.
* make changes in the text editor.
* save your changes by clicking 'Commit Changes'
    * on the confirmation screen, click 'Commit Changes'
 
</br>
</br>

1. Review the class definition below:
    ```c#
    public class Chair
    {
        public int Height { get; }
        public bool HasBack { get; }

        public Chair(int height, bool hasBack)
        {
            Height = height;
            HasBack = hasBack;
        }
    }
    ```
    Which of the following is NOT a valid way to create an instance of Chair? And why does this option not work?  
    A. `var bench = new Chair(24, true);`  
    B. `Chair bench = new Chair(24, true);`  
    C. `var bench = new(24, true);`  
    D. `Chair bench = new(24, true);`

   I believe that the correct answer is C, as all of the other options are telling the program to create a new instance of chair, but option C isn't mentioning anywhere what we are creating a new instance of, just naming it and telling us to create a new instance of something
   
    
    
3. Imagine you are interviewing for your first job.  The interviewer asks "What can you tell me about OOP?".  Write your response below:

OOP, or object oriented programming, is a model of computer programming that relies on objects to organize programs into simple and **reusable** pieces of code. OOP uses the process of instantation to create new instances of objects from a class definition by usng the keyword "new". You can create as many instances of an object as you want with OOP, thus making it very easily reusable, which is especially for larger projects. 

4. What is Automated Testing?

Automated testing is a seperate program that verifies the functionality of our primary program. An example of this would be Amazon having functions, such as make an order and take an order, being tested on an Amazon test site with tests like "verify that we can make an order" and "verify that we can take an order"

5. What are some benefits of creating tests for our projects?

There are a multitude of benefits to creating tests for our projects. One primary one is when working with bigger programs, such as at jobs we may have in the future, you may not be able to test your newly written code with a writeline or a full run if it relies on other pieces of information that you don't have. In this case, you would write tests to confirm the new addition to the program does exactly what it is supposed to do. Another benefit of creating tests is readability for future programmers who may be working on the code you wrote. They can see exactly how each behavior works based on the tests you performed. Testing also allows you to catch more things a user may do when using your program, so you can adjust for the mistakes they may make.

6. When you create a test project, you do not immediately have access to the class(es) in the project that you are testing.  What do you need to do in order to have access to those classes?

To have access to the classes, you will first right click on your unit tests folder in the solution explorer on the right side of the screen in VS. Then, youll scroll down to the "add" drop down menu, and select "project reference." finally, you will check the box of the class(es) you wish to have access to for testing, and you should be able to reference them to test them.

7. Take a look at the class below.  Write out the **names** of each test you would write to verify that this class is working. You do not need to write the whole test, just what you would **name** the test methods. Ex: `IsCreatedWithTwoArguments()`
```c#
    public class Vehicle
    {
        public int NumberOfWheels { get; }
        public string Color { get; private set;  }
        public int MilesDriven { get; private set; }

        public Vehicle(int numberOfWheels, string color)
        {
            NumberOfWheels = numberOfWheels;
            Color = color;
            MilesDriven = 0;
        }

        public string Summary()
        {
            string summary = $"This {Color} vehicle has {NumberOfWheels} wheels, and has driven {MilesDriven} miles.";
            return summary;
        }

// CreatesAndReturnsCarSummary

        public void Drive()
        {
            MilesDriven += 5;
        }

// DriveAddsMilesToCarAfterDriving

        public void Paint(string newColor)
        {
            Color = newColor;
        }

// PaintChangesCarPaintColor
    }
```



## Exercise (8 Points Possible)
In Visual Studio, clone your forked repository.  
In this solution, there is a `Vehicle` project and a `Vehicle.UnitTests` project.  The class in `Vehicle.cs` is complete, but the tests for that class are not yet finished.  Add tests to the `VehicleTests.cs` file so that all the methods and properties for the `Vehicle` class have tests.  When finished, there should be a minimum of 4 tests (one is already completed for you!).

### Submission

When the assessment is due, your instructors will show you how to commit the code you worked on in Visual Studio and push it up to GitHub :) 

### Rubric

This assessment has a total of **20 Points**.  Earning **10 or more** points is a **pass** and will indicate that you are progressing well with the material.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
