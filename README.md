# Croûte
Livecode test library for Levure that may resemble jest a bit. Let's see where this goes...

Croûte translated from French is crust. In keeping with Levure's bread and french theme, I thought croûte is a fitting name for a test library -- a key ingredient to a loaf of bread is yeast. A loaf of bread is only as good as it's crust! As you're baking your App, make sure you have a great crust (tests)!

Croûte is a testing framework written for Livecode intended for use as a Levure helper. The initial work essentially takes Trevore Devore's testing code for Levure. I'd like to see if we can have more of a BDD style to the project so I'm heading in a direction to make this look like jest. If you don't know what jest is don't worry. If you do, notice I said "look like".

### Project Status
As you can see, there is really nothing here yet. I'm working on an initial commit that will essentially be what is included in the current Levure framework for testing. I'll expand off of that once I get going.

### Using Croûte

Start a batch of related tests:

`describe name, fn`  

Create a test and execute it:

`test name, fn`

What we expect the test to do:

`expect(exp1, Matcher, exp2)`

Matchers are:

  `toBe` (tbd)
  
  `toEqual` (tbd)
  
  `toBeEmpty` (tbd)
  
  `toBeTrue` (tbd)
  
  `toBeFalse` (tbd)
  
  `not.` (tbd)
  
  `toBeGreaterThan` (tbd)
  
  `toBeGreaterThanOrEqual` (tbd)
  
  `toBeLessThen` (tbd)
  
  `toBeLessThenOrEqual` (tbd)
  
  `toMatch` (tbd)
  
  `toContain` (tbd)
  
  `toThrow` (tbd)
  
### Sample uses
This is the simplest way to test a value
  
```
...
  test "two plus two is four", "twoPlusTwoIsFour"
...
  
command twoPlusTwoIsFour
  expect(2+2, toBe, 4)
end twoPlusTwoIsFour
```
  
In this code, 2+2 is evaluated with the result being 4. The match "toBe" then compares to 4 to determine if the test succeeds.

You can also test the opposite of a matcher:
  
```
...
  test "adding positive numbers is not zero", "testForPositive"
...
  
command testForPositive
  repeat with a = 1 to 10
    repeat with b = 1 to 10
      expect(a+b, not.toBe, 0)
    end repeat
  end repeat
end testForPositive
```

In this test, the indexes a and b are added together with the results expected to not be 0. 
