# What is LOKI?
IOC Scanner that is open-source and free to use. Written by Florian Roth.   

Based on 4 methods one of which we are interested in:  
1. File Name IOC Check  
2. **Yara Rule Check**  
3. Hash Check  
4. C2 Back Connect check  

# How to use LOKI
[Neo23x0/Loki: Loki - Simple IOC and Incident Response Scanner (github.com)](https://github.com/Neo23x0/Loki)

## Syntax
```shell
# Getting Help
python loki.py -h 

# Updating 
python loki.py --update

# Scanning files rom within directory to be scanned
python ../path/to/loki.py -p . 
# alt
python loki.py -p path/to/directory/
```
