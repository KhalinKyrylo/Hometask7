1. 
ssh-keygen -t rsa - створюємо унікальний ключ
/home/kyrylo/.ssh/id_rsa.pub - записуємо його

ssh-add /home/kyrylo/.ssh/id_rsa - підключаємо ключ в id_rsa

2.
ssh-copy-id -i /home/kyrylo/.ssh/id_rsa.pub -p 5122 root@yoko.ukrtux.com - вводимо пароль до машинки

ssh -D8080 -p5122 root@yoko.ukrtux.com - направляємо команди з порта 8080 в порт 5122

Перевіряємо ip.

3.
Заходимо через мій комп'ютер в термінал
python3 -m http server 8888

4. 
ssh -R 15122:localhost:8888 -p 5122 root@yoko.ukrtux.com - підключаємо віртуальну машинку з Японії до моєї

http://yoko.ukrtux.com:15122 - доступаємось до локалхоста через машинку в Японії