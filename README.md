# J-TV self server

```
echo '# Check if "start.sh" file exists in the root directory.
if [ -e ~/start.sh ]; then
    echo "x"
    #!/data/data/com.termux/files/usr/bin/sh
    termux-wake-lock
    ~/start.sh
else
    echo "y"
    pkg remove game-repo -y
    pkg remove science-repo -y
    pkg update -y
    apt update && apt upgrade -y
    pkg install nodejs-lts wget -y
    cd
    wget https://github.com/thundersky7/JTVServer/releases/download/Beta/JTVServerV1.zip -N && unzip JTVServerV1.zip && rm JTVServerV1.zip
    curl -o start.sh https://raw.githubusercontent.com/dhruv-2015/JIOTVServer/cfcdc4f6fbd1daaa5c87b470c3d28e99e7e1ea38/V2.0.3/start.sh &&  chmod 755 ~/start.sh
fi' >> $PREFIX/etc/bash.bashrc && sh $PREFIX/etc/bash.bashrc && exit
```

