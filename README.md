# Raspberry_pi_bluetooth_setup_for_android

## If not done yet, do
sudo apt-get update

sudo apt-get upgrade

## Then

sudo apt-get install bluetooth blueman bluez

sudo reboot

## Install Python2 bluetooth 

sudo apt-get install python-bluetooth

## Install Python3 bluetooth 

sudo python3 -m pip install pybluez 

## in code include

server_socket=bluetooth.BluetoothSocket( bluetooth.RFCOMM )
 
port = 1

server_socket.bind(("",port))

server_socket.listen(1)

 
client_socket,address = server_socket.accept()

print "Accepted connection from ",address

while 1:
 
 data = client_socket.recv(1024)
 
 
client_socket.close()

server_socket.close()
