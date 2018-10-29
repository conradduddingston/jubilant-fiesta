# X-Team 118 Project Proposal Book.it

See https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code for tips on using *Markdown* tags to format __.md__ files

## Goal

Work as a team to create a project proposal for your X-team to complete together.
The project does not have to be extremely difficult,
but there must be work to do for each member of your team.
You may reference figures using "See figure 1".  
Be sure to submit corresponding image files, i.e. figure1.png (or figure1.jpg) for each figure.

## Grading: To earn full credit, your team's proposal must include:

* (md) documentation: [this file] describing purpose and use of your program

* Description of a program that has:

  ** a main Java program class in a file named Main.java
  
  ** a custom data structure designed and built by your team
  
  ** comprehensive testing of individual units
  
 Caution: You are not being asked to implement this program, at least not yet. 
 We just want your group to make a proposal or pitch for your program.
 
 Tip: Your custom data structure can be composed of or extensions of data structures that you have learned and used in previous programming assignments.  We're looking for decisions about how to build a high-level data structure that will likely have lower-level components.

## Problem Description

Briefly describe a problem that your team would like to solve.  
Describe at a high level a program that could solve that problem.

Problem:
- Textbooks are expensive. Perhaps we could build an application that uses a web scraper to gather information regarding pricing and availability of textbooks from a multitude of vendors and promptly returns this information in a easy-to-understand way.

## Questions to answer for Exercise #2

1. Name: Give your project proposal a name (and edit the top line of this file)
 Book.it


2. Output: Describe the output your program will produce.  Include and example format of the output produced.
Different online locations books are available for purchase or rent sorted by order of price. Links included.


3. Input: Describe the data that is needed to solve your problem. Include an example format of the input data.
Because our model is based off of simplicity, our platform would require only a title and whether or not the user is wishing to purchase or rent.

Example:
- The Art of Public Speaking Vol.3, buy

4. User Interface: Describe a user interface for your program.  Use text menus or a simple graphic user interface.
The user is presented with a simple, clean and appealing text interface where they are intended to input the title of a textbook. After searching, they are promptly presented with a list of potential online retailers sorted by price. The user then can jump from the app to their web browser should they select any of the found retailers.

5. Types List: Break your solution idea down into units that you think can be implemented with a single class.
Name each interface or class and briefly describe its function or purpose.

Input{
  Sting BookName
  Boolean isBuy
}

We will use inheritence for each of the retailers, with an abstract class RetailerScraper with operations that return data about the book we are searching for, and a subclass with the actual web-scraping implementation for each retailer. So BarnesAndNobleScraper would extend from RetailerScraper.

We would also need a RetailerResult Class{
   String RetailerName
   String URL;
   Double Price
}

The idea being that each Scraper would be provided with the instance of Input, and return a RetailerResult with the data about that book for that reailer. This data is then sorted and presented to the user.

Example:
Input input = new Input("The Art of Public Speaking, Vol 3", true);
RetailerResult result = BarnesAndNobleScraper.scrape(input);


## Edit and Submit this file and any figures referenced by this document.

