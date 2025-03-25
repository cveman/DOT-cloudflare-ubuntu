# DOT-cloudflare-ubuntu
1.1.1.1,1.0.0.1

sudo nano /etc/systemd/resolved.conf

Cloudflare: 1.1.1.1#cloudflare-dns.com 1.0.0.1#cloudflare-dns.com 2606:4700:4700::1111#cloudflare-dns.com 2606:4700:4700::1001#cloudflare-dns.com

DNSOverTLS=yes FallbackDNS= DNSSEC=yes Cache=no-negative

sudo systemctl enable systemd-resolved; sudo systemctl restart systemd-resolved; sudo systemctl restart NetworkManager; sudo resolvectl status;
