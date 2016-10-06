This project illustrates a bug in JSweet's code generation when the output is
set to AMD modules. Java-side imports from parent packages cause a failure at
require-load time. Requirejs' loader runs the code for the deepest package first,
which means the parent package has not yet populated it's exports object.
