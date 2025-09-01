https://drive.google.com/file/d/1CfX44tc_vVqBxnUeajjy5UeoGwekuY_I/view?usp=drive_link

# Dual.sh

pkg update && pkg upgrade -y

pkg install libjansson wget nano -y

wget https://raw.githubusercontent.com/TheRetroMike/PhoneMining/refs/heads/main/termux_vrsc_advc_dual.sh && chmod +x termux_vrsc_advc_dual.sh && \
./termux_vrsc_advc_dual.sh \
"stratum+ssl://solo-ap.luckpool.net:3958" "RDyw2vyGxkH5tx6i3Fj6nwro72xb7NrCFr" "Virtual1" "8" "0xf" \
"stratum+tcps://solo-asia.rplant.xyz:17149" "advc1q8ylgqj426smtre99lvz9yxkn3cavqfrgfhkzwa" "Virtual1" "8" "0xf0" && \
rm termux_vrsc_advc_dual.sh && ~/ui-startup.sh


#vers

pkg update && pkg upgrade

pkg install libjansson wget nano

mkdir ccminer && cd ccminer

wget https://raw.githubusercontent.com/Darktron/pre-compiled/generic/ccminer

wget https://raw.githubusercontent.com/Darktron/pre-compiled/generic/config.json

wget https://raw.githubusercontent.com/Darktron/pre-compiled/generic/start.sh

chmod +x ccminer start.sh

nano config.json

{
    "pools":
        [{
            "name": "NA-LUCKPOOL",
            "url": "stratum+tcp://ap.luckpool.net:3956",
            "timeout": 180,
            "disabled": 0
        }],

    "user": "RDyw2vyGxkH5tx6i3Fj6nwro72xb7NrCFr.Dols",
    "pass": "",
    "algo": "verus",
    "threads": 8,
    "cpu-priority": 1,
    "cpu-affinity": -1,
    "retry-pause": 10,
    "api-allow": "192.168.0.0/16",
    "api-bind": "0.0.0.0:4068"
}

~/ccminer/start.sh
