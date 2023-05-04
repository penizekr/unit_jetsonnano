# UniT 2023 - JetsonNano configuration  

- OS Ubuntu user name: tdi  
- OS Ubuntu password: tdi  
- VNC IP: 192.168.2.61   
- VNC password: tdi 
- Tested VNC viewer for W10: https://www.tightvnc.com/    
- Set VNC screen resolution via xterm: xrandr --fb 1280x1024 -display :0  
&nbsp;
- Info about JetsonNano: https://developer.nvidia.com/embedded/jetson-nano-developer-kit  
- This info: https://github.com/penizekr/unit_jetsonnano/edit/main/README.md

# wifi modem TP-Link TL-WN821N v6  

download and extract: https://github.com/Mange/rtl8192eu-linux-driver  
change in file "Makefile" : 
CONFIG_PLATFORM_I386_PC = n  
CONFIG_PLATFORM_ARM_AARCH64 = y  

run: make
run: sudo make install 

open file: sudo nano /etc/modules  
add into file:  
  8192eu  

  loop  

reboot JetsonNano  


