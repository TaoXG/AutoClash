**debian更换XanMod内核**
   ```bash
   wget -qO - https://dl.xanmod.org/archive.key | sudo gpg --dearmor -o /usr/share/keyrings/xanmod-archive-keyring.gpg
   ```
   ```bash
   echo 'deb [signed-by=/usr/share/keyrings/xanmod-archive-keyring.gpg] http://deb.xanmod.org releases main' | sudo tee /etc/apt/sources.list.d/xanmod-release.list
   ```
   ```bash
   sudo apt update && sudo apt install linux-xanmod
   ```
   ```bash
   echo 'net.core.default_qdisc = cake' | tee /etc/sysctl.d/90-override.conf
   ```

   
**一键安装AutoClash**   
   ```bash
   bash <(curl -sL https://ls.168828.xyz/autoclash)
   ```
