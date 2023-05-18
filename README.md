# Mod2 Week2 Assessment - James Cepriano

## Setup
1. Fork this repository.
1. Add ONE of the following GitHub profiles as a collaborator to your forked repo:
`memcmahon`, `rtillies`, `zoefarrell`
1. Clone your repo to your local machine.
1. Open your cloned repository in Visual Studio.
1. Insert your name on line 1 to replace `<YOUR NAME HERE>` above.

## Questions (10 Points Possible)
**Important** Answer these questions in this file on your `main` branch.  When finished with the questions, commit and push your main branch.  You do not need to create a pull request yet!

1. What does TDD stand for?

TDD stands for Test Driven Development. It is the process of writing out tests before creating the class for that test.

1. What are three benefits of using TDD?

a. Using TDD makes it more likely that a developer does not write code they don't need
b. It can help reduce the chance of creating bugs and make it unlikely that a finished program would be pushed out with a bug
c. Helps the developer plan out exactly what they want a class to do

1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?

When approaching a new program using the TDD process, I plan out what my code should accomplish and create unit tests that reflect what I want my classes to do in my program.

1. For the class below, outline the tests you would need.  Try to use as much C# syntax as possible. The first test has been provided for you. (this question is worth 4 points)
```c#
public class Dog
    {
        public string Name { get; }
        public string Breed { get; }
        public bool IsHungry { get; private set; }

        public Dog(string name, string breed)
        {
            Name = name;
            Breed = breed;
            IsHungry = true;
        }

        public void Eat()
        {
            IsHungry = false;
        }

        public void Sleep()
        {
            IsHungry = true;
        }

        public string Speak()
        {
            return "Bark Bark!";
        }
    }
```
```c#
// Add your tests here

[Fact]
public void DogHasNameAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
}

[Fact]
public void Dog_Eat_BoolOutputsFalse()
{
       Dog dog = new Dog("Nile", "Golden Retriever");
       dog.IsHungry = true;

       dog.Eat();

       Assert.Equal(false, dog.IsHungry);
}

[Fact]
public void Dog_Sleep_BoolOutputsTrue()
{
       Dog dog = new Dog("Nile", "Golden Retriever");
       dog.IsHungry = false;

       dog.Sleep();

       Assert.Equal(true, dog.IsHungry);
}

[Fact]
public void Dog_Speak_ReturnsString
{
       Dog dog = new Dog("Nile", "Golden Retriever");

       dog.Speak();

       Assert.Equal(dog.Speak, "Bark Bark!");
}

```

5. What is a merge conflict, and when might you encounter one?

A merge conflict is when a new version of a file can't be merged because the older and newer file have conflicting lines of code. You might encounter this when working on a program with multiple people.

1. You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.

We would create branches on our own systems and build the program in our branches. We would then commit changes we've made and push it to github. We would both create pull requests and fix any merge conflicts if there were any.
We would then merge the pull requests and pull the main branch to our computers.

1. Why is it good practice to have someone else approve and/or merge your PR?  

Someone else might find something in the pr that does not work or fit in the program. It would be better to have a second opinion on any code that has been written.
  
**Before moving on to the next section, commit your work and push your main branch!**
  
## Git Exercise (6 points possible)

1. Create a new branch called `elephants` (1 point)

1. Add the following to the end of the Animal Tracker file:

```
Elephants
- African Savanna
- Asian
- African Forest
```

3. Commit this change to the Animal Tracker file with an appropriate message. (1 point)

1. Create the following files with the listed contents:

**African Savanna.txt**
```
Average shoulder height: 2.6-3.2 meters
Average mass: 3.3-6.6 short tons
```

**Asian Elephant.txt**
```
Average shoulder height: 2.4-2.8 meters
Average mass: 3.0-4.4 short tons
```

**African Forest Elephant.txt**
```
Average shoulder height: 1.8-3.0 meters
Average mass: 2,000-7,000 kilograms
```

5. Add and Commit these new files with an appropriate message. (1 point)

1. Push your `elephants` branch to GitHub. (1 point)

1. Create a Pull Request in GitHub. Write a short description of the changes you made to the repo. (1 point) 

1. Request a review from your collaborator. (1 point)
  
## Submission

Submit the Assessment Submission form linked in your cohort slack channel!

## Rubric

This assessment has a total of 16 Points. Earning 11 or more points is a pass and will indicate that you are progressing well with the material.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
