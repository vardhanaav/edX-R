# edX-R
edX Course on R (2019)
# R - edX 2019 (Quick Ref Guide)

? <function> - help for that function
```sh
Eg: ? sqrt
```

Assignment: = and <-

## Vectors:
```sh
vect = c(1, 2, 3)
vect1 = c('A', 'E', 'I')
```
```sh
sequ = seq(0, 100, 2) or c(seq(0, 100, 2))
		   |   |   |
		   |  end  diff
		  start
```

## FUNCTIONS

1. *sqrt(number or sequence)* - gives square root for each element of the vector.
	```sh
	Eg: sqrt(100) or sqrt(sequence)
	```

2. *abs(number or sequence)* - gives the absolute value.

3. *mean(vector)* - Find the mean of a vector.
	```sh
	Eg: mean(vect1) 
	    mean(df$col)
	```

4. *sd(vector)* - Find the standard deviation. Same as mean

5. *seq(start, end, incr)* - creates a vector from start to end with each element differing by incr (similar to np.arange)

6. *min(vector)* - returns the minimum value 

7. *max(vector)* - returns the max of a vector

8. *str(df)* - Display the structure of an R object

9. *summary(df)* - Display the summary of an R object

10. *ls()* - list of variables

11. *read.csv(filename)* - Read filename

12. *write.csv(filename)* - Write to filename

13. *rm(var_name) or remove(var_name)* - remove a variable or a list of variables (comma separated)

14. *which.min(vector)* - return the index of the minimum value.

15. *which.max(vector)* - return the index of the max value.

16. *rbind(df1, df2) and cbind(df1, df2)* - combine to vectors or dataframes row-wise/column-wise. 

17. *View(df, title(optional))* - Invoke a spreadsheet-style data viewer on a matrix-like R object.

18. *plot(x, y, xlab, ylab)* - Plots a graph for x and y (which are R objects) and sets the x-label as xlab and y-label as ylab.

19. *nrow(x)* - no. of rows in x

20. *ncol(x)* - no. of columns in x

21. *hist(df$col)* - plot a histogram

22. *table(df$col_1, (optional)df$col_2...)* - table uses the cross-classifying factors to build a contingency table of the counts at each combination of factor levels. Length should be same.

23. *names(df)* - to get or set the name of an object.
    ```sh
	Eg: names(x)
		names(x) <- value
    ```
24. *tapply(df$col_1, df$col_2, op, (optional)na.rm = T)*: To remove na values, pass na.rm = T or TRUE
	a. Split the data by col_2
	b. Perform operation on col_1

25. *subset(DataFrame, condition)* - truncates the dataframe to the given condition
	```sh
	Eg: df_europe = subset(df, Region == "Europe") 
	```

26. match(x, table) - return a vector of indices where x is first found in table
	```sh
	Eg: match('Africa', df$Region)
		          |		    |
		          |	       vector
		    vector/value 
    ```

## DATAFRAMES

*df$new_col = c(1, 2, 3)* - Appends this vector to an already existing dataframe df.

    Eg: vect = df$col > mean(df$col, na.rm = T)

vect contains True of False based on the condition.

    vect = as.numeric(df$col > mean(df$col, na.rm = T))
    
now vect contains binary values.
