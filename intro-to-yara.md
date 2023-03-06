# Introduction
Every Yara command requires to arguments to be valid  
1. The rule file we create  
2. Name of file, directory or process ID to use the rule for  

Syntax:
`yara myrule.yar filetouserulefor`

Example of rule:  
```YARA
rule example{
        condition: true
}
```
Above rule will test if file you ran rule against exists.  

# Conditions
More conditions are available in the documentation. 

## Strings
Strings can be used to search for specific text or hecadecimal in files or programs. 



## Documentation
https://yara.readthedocs.io/en/stable/writingrules.html



