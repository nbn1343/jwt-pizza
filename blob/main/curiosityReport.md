# Curiosity Report: Selenium WebDriver

## Introduction

After working with Jest and Playwright, I was curious to find out what other testing frameworks there are available. I found information about Selenium and my wheels of curiousity began to turn as I decided to take a deep dive.

Selenium WebDriver is a web framework found within Selenium which is a suite of tools that are widely used in the testing community when it comes to cross-browser testing. Specifically, Selenium Webdriver is the core component of Selenium which provides a programming interface for driving the web browsers. It allows to write tests in different programming languages to interact with the web elements, simulate user interactions and perform assertions.

I am curious to see what benefits Selenium WebDriver has and how it compares to PlayWright and Jest.

## Understanding Selenium Webdriver

Selenium WebDriver, created by Simon Stewart in 2006, was the first cross-platform testing framework that could control browsers at the operating system level. It acts as an interpreter between your code and different browser drivers, allowing direct browser interaction. As a W3C recommendation from the Browser Testing and Tools Working Group, WebDriver has established itself as an industry standard for browser automation.

## Architecture and Working Principles

WebDriver Architecture is made up of four major components:

1. Selenium Client library
2. JSON wire protocol over HTTP
3. Browser Drivers
4. Browsers

From what I discovered, when you run a Selenium test, commands are sent as HTTP requests, with responses received in JSON format. With this architecture design, Webdriver is enabled to interact with multiple browsers across different operating systems. This makes it highly versatile for cross-browser testing.

## How to use Selenium WebDriver in Java: Example

```
import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;

import org.testng.Assert;

import org.testng.annotations.Test; 

public class BrowserStackDemo { 

   WebDriver driver;  

   @Test

   public void verifyTitle() {

         driver= new ChromeDriver();

         driver.get("https://www.browserstack.com/");

         Assert.assertEquals(driver.getTitle(), "Most Reliable App & Cross Browser Testing Platform | BrowserStack");

         driver.quit();

   }

}
```

## Benefits of Selenium WebDriver

- Cross-browser compatibility: It is one of the most popular Open-Source tools and is easy to get started with for testing web-based applications. It also allows you to perform cross browser compatibility testing.
- OS Support: Supports multiple operating systems like Windows, Mac, Linux, Unix, etc.
- Language Support: It provides compatibility with a range of languages, including Python, Java, Perl, Ruby, etc.
- Browser Support: Provides support for modern browsers like Chrome, Firefox, Safari, and Internet Explorer.
- Quick Execution: Selenium WebDriver completes the execution of test scripts faster when compared to other tools
- Concise API: More Concise API (Application Programming Interface) than Selenium RC’s
- Supports specialized WebDriver implementations: It also provides compatibility with iPhoneDriver, HtmlUnitDriver, and AndroidDriver

## Conclusion

After researching Selenium WebDriver, it is apparent that it remains a leading choice for automated browser testing thanks to its broad language, browser, and operating system support. Unlike Jest, which is focused on fast unit and integration testing for JavaScript/TypeScript code, and Playwright, which excels at modern, fast end-to-end testing for web apps, Selenium WebDriver is uniquely positioned for projects that require extensive cross-browser compatibility and support for legacy systems.

Now knowing Jest and Playwright, as well as this deep dive into Selenium WebDriver, I feel that I could comfortably use them when developing in the real world.