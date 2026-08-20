# What keyword arguments are

Keyword arguments pass values to parameters by name rather than by position. In languages that support this feature, keyword arguments can make calls clearer because each value is labelled with the parameter it targets.

# Positional vs keyword calls

When providing positional arguments (which is what you have probably mostly seen so far), the order of the arguments dictates which parameter they are assigned to: the first argument goes to the first parameter, the second to the second, and so on. With keyword arguments, however, we specify the name of the parameter we want to assign a value to. This allows for more readable and maintainable code, especially when dealing with functions that have many parameters.

Exact syntax will vary by language, but the example below demonstrates the concept:

```
FUNCTION describe_person(name, role, country)
    RETURN name + " - " + role + " - " + country
END FUNCTION

PRINT describe_person("Ada", "Engineer", "UK") // Positional call, returns "Ada - Engineer - UK"
PRINT describe_person(role="Engineer", country="UK", name="Ada") // Keyword call, returns "Ada - Engineer - UK"
```

# Keyword Arguments and Optional Arguments

Keyword arguments are particularly useful when combined with optional arguments, as they allow for the specification of some parameters without having to provide values for all of them. For example:

```
FUNCTION describe_person(name, role="UNSET", country="UNSET")
    RETURN name + " - " + role + " - " + country
END FUNCTION

PRINT describe_person("Ada", country="UK") // Returns "Ada - UNSET - UK"
```

In the example above, the use of keyword arguments allows us to provide a value for `country` without specifying `role`.
