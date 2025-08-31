https://drive.google.com/file/d/1CfX44tc_vVqBxnUeajjy5UeoGwekuY_I/view?usp=drive_link
# Dual.sh
pkg update && pkg upgrade -y

pkg install libjansson wget nano -y 

wget https://raw.githubusercontent.com/TheRetroMike/PhoneMining/refs/heads/main/termux_vrsc_advc_dual.sh && chmod +x termux_vrsc_advc_dual.sh && ./termux_vrsc_advc_dual.sh "stratum+tcp://ap.luckpool.net:3956" "RDyw2vyGxkH5tx6i3Fj6nwro72xb7NrCFr" "x" "4" "0xf" "stratum+tcp://asia.rplant.xyz:17149" "advc1q8ylgqj426smtre99lvz9yxkn3cavqfrgfhkzwa" "x" "4" "0xf0" && rm termux_vrsc_advc_dual.sh && ~/ui-startup.sh
