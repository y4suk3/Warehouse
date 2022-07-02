# elabftw 構築

## 環境
- Ubuntu 22.04 TLS

## インストール
1. sudo apt update
2. sudo apt install curl docker-compose dialog borgbackup
3. sudo usermod -aG docker $USER
4. curl -sL https://get.elabftw.net -o elabctl && chmod +x elabctl
5. sudo mv elabctl /usr/local/bin/
6. sudo ln -s /usr/bin/python3.10 /usr/bin/python
7. sudo su
8. elabctl install
9. elabctl start
10. docker exec -it elabftw bin/install start
    
DB への Conection error ができるので、`docker exec -it elabftw bash` でログインしてから、`./bin/install start`だとうまくいく。