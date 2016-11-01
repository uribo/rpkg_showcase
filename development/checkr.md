

# checkr: Automatically Test R Functions

[![](http://www.r-pkg.org/badges/version/checkr)](http://cran.rstudio.com/web/packages/checkr/index.html)

- CRAN: http://cran.r-project.org/web/packages/checkr/index.html
- GitHub: https://github.com/peterhurford/checkr


```r
> library(checkr)
```

バージョン: 0.1.4

-----



| 関数名 | 概略 |
|--------|------|
| `%contains%` | Test if a list contains some elements of the desired class. |
| `%is%` | Test for class membership |
| `%within%` | Define if a number is within a certain range. |
| `ensure` | Ensure checks that certain preconditions and postconditions of a function are true. |
| `force_reload_test_objects` | Function to force reload the test object cache, if needed. |
| `function_name` | Get the name from a passed function, which may be a validated function or just a block. |
| `function_test_objects` | Create the necessary testing objects to quickcheck a function. |
| `get_prevalidated_fn` | Get the pre-validated function that is wrapped in validations. |
| `installed_dataframes` | Get all the user-installed dataframes through data() |
| `is.empty` | Tests whether an object is empty. |
| `is.simple_string` | Tests whether a string is simple. |
| `is.validated_function` | Determine whether a function is checked with checkr. |
| `list_classes` | Get all the classes within a list. |
| `package_exports_checked` | Checks if all exported functions in the package are checked using checkr. |
| `postconditions` | Get the stated postconditions of a validated function. |
| `preconditions` | Get the stated preconditions of a validated function. |
| `present` | Tests whether an argument to a function is present. |
| `print.validated_function` | Print validated functions more clearly. |
| `print_args` | Print function arguments |
| `quickcheck` | Quickcheck a function. |
| `random_matrix` | Generate a random matrix. |
| `random_objs` | Generate a vector or list of random objects from a particular set of possible choices. |
| `random_simple_strings` | Generate a random simple string (i.e., a length-1 non-empty vector of characters). |
| `should_be_checked` | Determine whether a function ought to be checked with checkr. |
| `test_objects_` | Generates random R objects to be put into functions for testing purposes. |
| `validate` | Validate checks that certain facts are true. |
| `validate_` | Validate without NSE. |

------

## ensure


```r
> add <- ensure(
+   pre = list(x %is% numeric, y %is% numeric),
+   post = result %is% numeric,  # `result` matches whatever the function returns.
+   function(x, y) x + y)
```

```
Error: At least one condition is needed to ensure value.
```

```r
> add(1, 2)
```

```
Error in (function (classes, fdef, mtable) : unable to find an inherited method for function 'add' for signature '"numeric", "numeric"'
```



