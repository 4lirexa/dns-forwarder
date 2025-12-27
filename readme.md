آموزش راه‌اندازی:
https://sajadabdollahi.ir/posts/bypass-sanctions/

VPS_IP=x.x.x.x envsubst < dnsmasq/proxy.conf.template > dnsmasq/proxy.conf


Port Already in use:
sudo systemctl stop systemd-resolved
sudo systemctl disable systemd-resolved
sudo systemctl mask systemd-resolved  # prevents accidental start

# Fix resolv.conf (create a static one)
sudo rm /etc/resolv.conf
echo -e "nameserver 1.1.1.1\nnameserver 1.0.0.1" | sudo tee /etc/resolv.conf


Credit: https://github.com/M-Ahadi/dockers
