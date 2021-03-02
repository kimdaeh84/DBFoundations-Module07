** Author ** Daehoon Kim
** Date ** 2.28.21

# ASSIGNMENT 07: SQL FUNCTIONS 
## INTRODUCTION
The purpose of this paper is to describe to how to use SQL functions and some of different types of functions a database developer or user can utilize.  The topics that will be covered are when to use a user defined function (UDF) and the differences between scalar, inline, and multi-statement functions.  

## WHEN TO USE A SQL UDF
A UDF allows a user to create custom calculations in code that accepts parameters, does actions and returns the result values. The result either is a Table form or a single value. UDFs can be used in scripts, Stored Procedures, or other UDFs within a database.  A user would use an MDF to allow a user to create the function, store it within the database, and reference it within the with the code. User-defined functions can be modified independently of the program source code.

## DIFFERENCES BETWEEN SCALAR, INLINE, AND MULTI-STATEMENT FUNCTIONS
There are three major types of UDFs a user can utilize in a database: Scalar, Inline, and Multi-Statement function. While each has its own purposes, the differences highlight when a user would utilize each UDF type.  
Scalar: The return syntax accepts one or more parameter but return only one value.  Additionally, the return function can utilize logic such as IF blocks or WHILE Loops and refer to other functions within the syntax.  Scalar functions do utilize BEGIN/END Statements, and they cannot update data in the underlying tables. (See Figure 1 for Scalar Function)
 
Figure 1 shows the structure of the Scalar Function.  Scalars can utilize multiple parameters and BEGIN/END, but returns one value
Inline: The return table and its definition will be based on the function statement.  There would not be any need to specify the structure of the return table.  Inline functions do not utilize the BEGIN/END syntax, and they allow users to update the data of the table. (See Figure 2 for Inline Function Structure)
 
Figure 2 shows the structure of the Inline Function.  Inline Function can utilize multiple parameters within the function’s return statements and may update the data of the table.
Multi-Statement: The return syntax defines the structure of the return table.  Declaring the table variable that will be used to store and accumulate the rows are returned as the value of the function.   The multi-statements do utilize BEGIN/END Syntax and they cannot update data the underlying tables. (See Figure 3 for Multi-Statement Function Structure)
 
Figure 3 shows the structure of the Multi-Statement Function. Multi-Statement Table-Valued Function body can contain more than one statement. The structure of the table is returned from the function that can be defined by us.  

## CONCLUSION
In this paper, I intended to describe how to use SQL functions and some of different types of functions a database developer or user can utilize.  The topics that were covered were when to use a user defined function (UDF) and the differences between scalar, inline, and multi-statement functions.  
