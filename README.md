# Ruby Instance Variable Assignment Bug

This repository demonstrates a common error in Ruby related to assigning values to instance variables without explicitly defining setter methods.  The `bug.rb` file shows the code that produces the error, while `bugSolution.rb` shows the corrected code.

## Bug Description

In Ruby, if you only define a getter method for an instance variable (using `attr_reader` or by simply defining a method that returns the instance variable), you cannot directly assign a new value to that variable using the assignment operator (`=`).  This results in a `NoMethodError`. The error arises because Ruby doesn't automatically generate setter methods.

## Solution

The solution is to explicitly create setter methods using `attr_writer`, `attr_accessor` (which creates both getter and setter methods), or by manually defining the setter method.