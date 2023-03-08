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

Example where we search a directory for all files containing "Hello World!"  
```YARA
rule helloworld_checker
{
    strings:
        $hello_world = "Hello World!"
        
    condition:
        $hello_world
}
```

## Operators and Keywords  
If we have multiple conditions we can use operators or keywords  
`<` Less than  
`>` Greater than  
`=` Equal to  
`<=` Less than or equal to  
`>=` More than or equal to  
`!=` Not equal to  
`any of them` Will check if any condition matches  
`and` Will check if both conditions matches  
`not` Check if condition do NOT match  
`or` Check if one or both of the condition matches  

Example where we check multiple conditions:   
```YARA
rule helloworld_checker
{
    strings:
        $hello_world = "Hello World!"
        
    condition:
        $hello_world and filesize <= 15KB        
}
```

## Meta
Under metadata section we can put additional information about our rule. 
We can put information such as Author, Date, Description etc 

Example of rule with meta section: 
```YARA
rule Metaexample
{
    meta:
        desc = "Rule that checks for the Hello World! string in files"
        author = "Tw3lly"
        
    strings:
        $hello_world = "Hello World!"
        
    condition:
        $hello_world     
}
```




## Documentation
https://yara.readthedocs.io/en/stable/writingrules.html

## Cheatsheet
https://blog.securitybreak.io/security-infographics-9c4d3bd891ef#18dd



