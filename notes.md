# Notes — Week 3

## Regular expressions (Regex)

* I used Visual Studio Code for this section. It has the same `.*` toggle for regex as Sublime Text.
* Like a lot of people, I haven't fully learned regular expressions to a point that I remember much of the syntax. I usually do a web search when I need to know something about regular expressions.

### Basic principles

* I don't have anything to note regarding these, but I'll refer to this section of the instructions again or other online resources if I forget something. I don't feel the need to repeat any of the ideas here.

### Letters of the Republic of Texas

* I've used `curl` in the past. I guess it has some overlap with `wget` with what it can do.
* Downloading the file was quick; only about 2 MB of text.
* Getting the file contents down to just the table required deleting over 53,000 lines!
* Visual Studio Code gave me the error:
    > "Invalid regular expression: /(.+\<to\>)/: Invalid escape

    Rather than figure out the differences, I switched to using Sublime Text for this exercise and it worked fine.
* That was a good exercise. I think I fixed most or all of the extra comma errors correctly.

## OpenRefine

* I don't think I've heard of this tool before. If I have, it was a long time ago.

## Installation

* I didn't experience any issues setting up OpenRefine.
* It's nice that OpenRefine's ZIP just came with the executable on Windows. Not much installation required.
* The fact that it runs like a server is pretty cool, but is it necessary?
  * I guess it could be applied in a way that allows you to access the tool from other systems on your network if you went through the trouble of configuring things that way. It could also have to do with how the developer felt like programming it, but generally, one should select technologies based on the problem at hand. Nonetheless, I think they knew what they were doing.

### Cleaning and reconciling names

* I didn't refer to the video when following these steps.
* The data loaded from the CSV seemed to display correctly.
* This is a pretty useful and effective tool.
* I reduced the unique Senders to 157. With the "nearest neighbor" method, turning up the block radius and turning down the block chars helped catch duplicates that the default settings missed.
* I reduced the unique Recipients to 172.
* The automatic whitespace removal did nothing for Senders, but affected 990 cells in Recipients.

## Network analysis

### Databasic.io

* I don't think the instructions ever suggested to drop the date column, so this won't initially be possible. 
* I used Excel to drop the date column and change the header row to say source,target.
* Uploading a file in the current format kept yielding "Internal Server Error" on ConnectTheDots, so I'll have to try again later.
  * From the screenshot, it looks like a useful visualization.

### More complex visualizations and analysis

* When web technologies like Databasic.io fail, we've got offline technology like Gephi as a backup.
* I needed to install Java 1.8 to use Gephi.
* Installing Java 1.8 didn't do the trick either, but I found [here](https://github.com/gephi/gephi/issues/1787#issuecomment-498979393) that launching the 32-bit executable does the trick. It worked!
* Some of these spreadsheet import options are familiar, similar to ones in Excel.
* It worked!

![It worked!](https://i.imgur.com/KOyIkho.jpg "It worked!")  
*It worked!*    

### Navigating Gephi

* While I've worked with graph theory a bit, I don't think I'd want to develop software like this. Seems pretty useful, though.
* I let the force-directed layout run for at least 7 minutes before stopping it. Though I noticed change over time, I only screenshotted the end result:

![End result of force-directed layout](https://i.imgur.com/jx3Ei30.jpg "End result of force-directed layout")
*End result of force-directed layout*

* Connected Components returned 27.
* I might have also applied the colour gradient based on PageRank.
* Ahhhh, that all came together with the step that added labels. This is pretty useful software and not all that hard to understand, after all.

![Final preview](https://i.imgur.com/trWkwZu.jpg "Final preview")  
*Final preview*

### [Network Analysis in Python](https://programminghistorian.org/en/lessons/exploring-and-analyzing-network-data-with-python)

* This is quite the lengthy tutorial, so this is my note to try it later when I've more time. A quick skim through it suggests it's worth it!

## Bonus

* This week's bonus looks like another fun demo of pasting stuff into an R script, studying how each line works, and then observing what it does!
* Most interesting R script yet.
* I was able to figure out how to write commands to write the hub score and authority scores to files, basing it off earlier commands in the script.

> Examine that file — what groups do you spot? What might these mean, if you went back to the content of the original letters?

I didn't analyze the content of the original letters too closely, but I would imagine these groups (in cfg.csv) are people in different cities, and the numbers are simply an index of people in those cities (one-indexed).

![A plot generated in R Studio](https://i.imgur.com/yE7tWxy.jpg "A plot generated in R Studio")  
*A plot generated in R Studio*

![Another plot generated in R Studio](https://i.imgur.com/NzOkbGh.jpg "Another plot generated in R Studio")  
*Another plot generated in R Studio*
