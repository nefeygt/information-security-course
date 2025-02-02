# h3 Hello Lab

## x) Read/watch/listen and summarize:
1. Install Debian on Virtualbox - Updated 2024:
   - I followed the guide step-by-step and succesffuly set my Debian up.
   - Everything is working as intended.
   - I also installed the drivers (guest additions) for better resolution.
2. Command Line Basics Revisited:
   - I revisited the basic Linux commands such as: pwd, ls, cd, lessü | (pipe), nano, mkdir, mv, cp, rmdir, rm, rm -r, ssh, exit, man, wget, history, sudo, dpkg, 
   - I learned these new: scp
   - I learned the important directories: /, /home/, /home/tero/, /etc/, /media/, /var/log/
   - I used the commands and practiced them.
   - I downloaded nethack and saw that it runs, then I deleted it.

## a) Can't fish:
1. ping 1.1.1.1 (connected to the internet):
   -![image](https://github.com/user-attachments/assets/a56711ec-9184-4c92-a537-cdf9623bdcfa)
   -Ping is basically packets called ICMP Echo request, in the screenshot there are several fields:
      -icmp_seq: sequence of the ping packets in that whole ping function
      -ttl: means time-to-live, total number of hops before dropping a packet
      -time: total time of the ping packet starting from sending and ending in recieving
   -I learned these words in my networking course last year.
3. ping 8.8.8.8 (connected to the internet):
   -![image](https://github.com/user-attachments/assets/a85287a1-1cf4-4ad6-aba8-fd87ace66722)
4. When disconnected from the internet:
   -![image](https://github.com/user-attachments/assets/ee7d51b9-87ba-4c93-9709-a49c68b11297)
   -It is not possible to send pings without the internet connection.


## b) Local only:
## c) Daemon scan:
## d) Bandit oh-five:
## e) Voluntary bonus task:


### References:
Karvinen 2024: Information Security Course, https://terokarvinen.com/information-security/ <br>
Karvinen 2021: Install Debian on Virtualbox - Updated 2024 <br>
Karvinen 2020: Command Line Basics Revisited
