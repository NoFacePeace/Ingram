```
python3 -m venv path/to/venv      
cd ips
masscan -p80,8000-8008 -iL cn.txt -oL cn.masscan --rate 800000  
grep 'open' cn.masscan | awk '{printf"%s:%s\n", $4, $3}' > cn.targets.txt

grep 'open' tmp.masscan | awk '{printf"%s:%s\n", $4, $3}' > tmp.targets.txt
 source path/to/venv/bin/activate

 python run_ingram.py -i japan.targets.txt -o japan 

 python run_ingram.py -i ips/tmp.targets.txt -o tmp

 export OBJC_DISABLE_INITIALIZE_FORK_SAFETY=YES
 
```