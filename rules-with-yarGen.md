# Generating rules with yarGen
yarGen is a generator for YARA rules  
Created by Florian Roth  
[Neo23x0/yarGen: yarGen is a generator for YARA rules (github.com)](https://github.com/Neo23x0/yarGen)  

## Syntax and usage
```shell
# Updating 
python3 yarGen.py --update

# Generating Rules
python3 yarGen.py -m /home/user/sus-file/susfile1 --excludegood -o /home/user/yara-rules/generatedrule.yar

-m specified path for file you want to generate rule for
--excludegood will exclude all goodware strings
-o path/name for output 
```

