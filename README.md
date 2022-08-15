# Simple-Selenium-Test-using-TestNG
Assignment 2 W10D1 - SDA - Software QA Bootcamp


## Table of contents
* [Question](#question)
* [Answer](#answer)
* [Output Screenshots](#output-screenshots)

---
## Question
- STEP 1: Try to log in using any of your favorite websites with the wrong username or password
- STEP 2: Enter a wrong password or username
- STEP 3: Assert the error message received using TestNG

---

## Answer
I used [Instagram](https://www.instagram.com/?hl=en) website
Before running the code, there are some steps that need to take considered:

### First:
Setup Latest [Web Driver](https://chromedriver.chromium.org/downloads) for Chrome Driver. 

Donwload the necessary jar files:
- [Selenium](https://www.selenium.dev/downloads/) (Lastest).
- [TestNG](http://www.java2s.com/Code/Jar/t/Downloadtestng685jar.htm)  (Lastest).
- [jcommander](http://www.java2s.com/Code/Jar/j/Downloadjcommanderjar.htm)  (Lastest). 

### Second:
Add them as a library in the classpath of the project
- _click-reight on the file project >Build path > configure Bild path > Java Build Path > Libraries > classpath > add external JARs > Apply and close_.

### Third:
I opened the website, then take web elements, and then add them to the code.

I used `AssertEquals()` method to compare the actual and expected results. If both the actual and expected results are same, then the assertion pass with no exception and the test case is marked as "passed".

```md
WebElement error = driver.findElement(By.xpath("//p[contains(@role,'alert')]"));
if (error.isDisplayed()) {
    String text = error.getText();
    Assert.assertTrue(true, text);
	}
```

---

## Output Screenshots:

<p align="center">
<img src="https://user-images.githubusercontent.com/48597284/184711100-e8df44a5-d6ac-4cd6-902c-d75292c74e91.png" width=80% height=80%>

https://user-images.githubusercontent.com/48597284/184711021-8689df1a-fe0d-4e6b-a833-24fea8bf3c71.mp4

</p>
