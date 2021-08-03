# Simgo TC


* tc q add dev wlan0 root handle 23:  htb  default 14

  * tc c add dev wlan0 parent 23:  classid 23:1 htb rate %THRESHOLD%kbit overhead 32

    * tc c add dev wlan0 parent 23:1 classid 23:14 htb prio 3 rate %RATE%kbit ceil %THRESHOLD%kbit overhead 32

      - tc q add dev wlan0 parent 23:14 handle 14:  htb

    - tc c add dev wlan0 parent 23:1 classid 23:13 htb prio 0 rate %RATE%kbit ceil  %THRESHOLD%kbit overhead 32

      - tc q add dev wlan0 parent 23:13 handle 13:  htb

    - tc c add dev wlan0 parent 23:1 classid 23:15 htb prio 4 rate 50kbit ceil 50kbit  overhead 32

      - tc q add dev wlan0 parent 23:15 handle 15:  htb

  - tc f add dev wlan0 parent 23:  protocol ip prio 0 u32 match ip dport 53 0xff flowid 23:13


