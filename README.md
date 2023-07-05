### debian更换XanMod内核

- **注册PGP密钥**
   ```bash
   wget -qO - https://dl.xanmod.org/archive.key | sudo gpg --dearmor -o /usr/share/keyrings/xanmod-archive-keyring.gpg
   ```
- **添加仓库**
   ```bash
   echo 'deb [signed-by=/usr/share/keyrings/xanmod-archive-keyring.gpg] http://deb.xanmod.org releases main' | sudo tee /etc/apt/sources.list.d/xanmod-release.list
   ```
- **安装**
   ```bash
   sudo apt update && sudo apt install linux-xanmod
   ```
- **在systemd（> = 217）的系统中使用CAKE队列规则**
   ```bash
   echo 'net.core.default_qdisc = cake' | tee /etc/sysctl.d/90-override.conf
   ```
- **重启**
   ```bash
   reboot
   ```
- **查看生效**
   ```bash
   sysctl net.core.default_qdisc
   ```
   ```bash
   sysctl net.ipv4.tcp_available_congestion_control
   ```
   ```bash
   sysctl net.ipv4.tcp_congestion_control
   ```

### 一键安装AutoClash
   ```bash
   bash <(curl -sL https://ls.168828.xyz/autoclash)
   ```
