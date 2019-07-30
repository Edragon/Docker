1. Build it, -t tag test    
docker build -t test .

2. Run it  
docker run -it --name "test" test:latest bash 


3. Enter into docker test and may still need to run following commands  
 export IDF_PATH=/ESP8266_RTOS_SDK  
 export PATH="$PATH:/xtensa-lx106-elf/bin"  

4. Build test  
Cd /ESP*/e*/g*/p*/  
Make all 
