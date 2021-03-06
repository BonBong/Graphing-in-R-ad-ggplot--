---
output: word_document
---
#SWIRL base R Tutorial Notes

* The command _range()_: min and max values. Use theboolean _na.rm =TRUE_ to exclude any "NA" data/cells.
* histogram funtion: hist(_data.set $ y.variable_)
* boxplot function: boxplot(_y.variable $ x.variable_)
* 2-D scatter plot: plot(_data.set $ variable, data.set $ variable_).
	+ **OR** to avoid eschew this long notation: with(_data.set, plot(x.variable, y.variable)_)
* either 
* to get plot dimensions in inches: par()$pin OR par("pin")
*  The par() function is used to specify global graphics parameters that affect all plots in an R session. (Use
dev.off or plot.new to reset to the defaults.) These parameters can be overridden when specified as arguments to specific plotting functions. These include las (the orientation of the axis labels on the plot), bg (background color), mar (margin size), oma (outer margin size), mfrow and mfcol (number of plots per row, column).
* To add lines, you give a vector of x values and a corresponding vector of y values (or a 2-column matrix); the function lines just connects the dots. The function text adds text labels to a plot using specified x, y coordinates.
* type set to 'n' tells R to plot, but without the data in it.
* the commans _subset(x,..) returns sections of vectors, matrices that have been outlined
* Use the points command to edit the point graphics
* Now we'll use the R command legend to clarify the plot and explain what it means. The function has a lot of arguments, but we'll only use 4. The first will be the string "topright" to tell R where to put the legend. The remaining 3 arguments will each be 2-long vectors created by R's concatenate function, e.g., c(). These arguments are pch, col, and legend. The first is the vector (17,8),
 the second ("blue","red"), and the third ("May","Other Months").
* Use par with the parameter mfrow set equal to the vector (1,2) to set up the plot window for two plots side by side. The result is only visible once new plots have been added.
	+ This one with 3 plots, to illustrate inner and outer
| margins. First, set up the plot window by typing par(mfrow
| = c(1, 3), mar = c(4, 4, 2, 1), oma = c(0, 0, 2, 0))
	+ Margins are specified as 4-long vectors of integers. Each
| number tells how many lines of text to leave at each side.
| The numbers are assigned clockwise starting at the bottom.
| The default for the inner margin is c(5.1, 4.1, 4.1, 2.1)
| so you can see we reduced each of these so we'll have room
| for some outer text.
	+ As each plot should have its own title, a main title for the overall plots has to be added. This is done using the comman **mtext()**. Call the **mtext** command with the string detailing the overall title and set the argument outer equal to TRUE.
