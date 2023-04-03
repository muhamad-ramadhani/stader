<p style="font-size:14px" align="right">
<a href="https://t.me/PemulungAirdropID" target="_blank">Join our telegram <img src="https://user-images.githubusercontent.com/72949170/194228482-0f875615-e155-4b12-8716-8111addd6cba.jpg" width="30"/></a>
</p>

<p align="center">
  <img width="60%" height="auto" src="https://user-images.githubusercontent.com/72949170/229575666-f9e0d028-b3e0-4a0b-b216-86b516875f8b.png">
</p>

# STADER TESTNET

|  Komponen |  Persyaratan Minimum |
| ------------ | ------------ |
| CPU  | 4 core  |
| RAM | 16 GB  |
| Penyimpanan  | 2 TB HDD |
| Koneksi | 10 Mbit/s |

Website
> https://www.staderlabs.com/

Social Media
> [ Discord ](https://discord.gg/staderlabs) | [ Twitter ](https://twitter.com/staderlabs)

## 1. Install Docker (Kalau udah ada bisa skip)
- Update & Install 
```
sudo apt-get update
sudo apt-get install \
  ca-certificates \
  curl \
  gnupg \
  lsb-release
  ```
- Install GPG Docker
```
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
- Setup Repository
```
echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
- Install Docker
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

## 2. Install Node
```
wget https://dub.sh/linuxamd64 -O ~/bin/stader-cli
```
- Ke directory bin
```
cd $HOME/bin
```
- Jadikan Executable File
```
chmod +x ~/bin/stader-cli
```
- Restart Terminal
```
bash
```
- Install Service
```
stader-cli --allow-root service install
```
- Run Wizard Node
```
stader-cli --allow-root service config
```

Akan muncul menu, follow step by step
- Goerli Network
- Locally managed
- System-recommended
- System-recommended
- Isi moniker/graffiti/usernamemu (bebas)
- https://beaconstate-goerli.chainsafe.io/
- Yes
- No
- Yes
- Locally managed
- Pilih regulated terus next
- Save and exit
- y
- y

Sync memakan waktu 1-3 Hari (Tunggu sampai selesai sebelum ke step selanjutnya)

## 3. Create Validator
- Cek sync
```
stader-cli --allow-root node sync
```
Jika muncul seperti di bawah, berarti sudah sync
> Your primary execution client is fully synced.

- Buat Wallet 
```
stader-cli --allow-root wallet init
```
Jangan Lupa untuk Backup

- Claim Faucet
1. Ke [ Discord ](https://discord.gg/staderlabs) Mereka
2. Ke ```#ethxclusives-permisionless-node-operators```
3. Type !interested
4. Tunggu dapet role ```beta tester```
5. Masuk ke channel ```#ethx-rolling-beta-test```
6. Paste Node key 

- Create Validator
```
stader-cli --allow-root node register --on <MONIKER>
```
Ganti MONIKER menjadi terserah kalian (ga pakai <>)

- Deposit SD Token
```
stader-cli --allow-root node deposit-sd --amount 640
```

- Deposit ETH
```
stader-cli --allow-root node deposit --num-validators 1
```

- Cek Status
```
stader-cli --allow-root node status
```

## DONE, UNTUK UPDATE SELANJUTNYA KALIAN BISA PANTAU <a href="https://t.me/PemulungAirdropID" target="_blank">CHANNEL KITA </a>

## Perintah Berguna
- Cek Status Service
```
stader-cli --allow-root service status
```

- Cek Logs Service
```
stader-cli --allow-root service logs
```

- Cek Status Node
```
stader-cli --allow-root node status
```

