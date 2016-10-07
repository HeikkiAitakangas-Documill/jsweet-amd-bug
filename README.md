This project illustrates a bug in JSweet's 1.1.x code generation when the output is
set to AMD modules. Java-side imports from parent packages cause a failure at
require-load time. Requirejs' loader runs the code for the deepest package first,
which means the parent package has not yet populated it's exports object.

This bug is not relevant anymore in JSweet >= 1.2 since module generation strategy was full reworked.