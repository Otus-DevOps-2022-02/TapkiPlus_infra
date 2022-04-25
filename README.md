# TapkiPlus_infra
TapkiPlus Infra repository

ssh -A -i /root/.ssh/ssh_tapkiplus.key -J appuser@51.250.2.14 appuser@10.128.0.17

cat ~/.ssh/config
Host someinternalhost
	HostName 10.128.0.17
	ProxyJump %r@51.250.2.14
	IdentityFile /root/.ssh/ssh_tapkiplus.key
	User appuser

bastion_IP = 51.250.2.14
someinternalhost_IP = 10.128.0.17

yc compute instance create   --name reddit-app   --hostname reddit-app   --memory=4   --create-boot-disk image-folder-id=standard-images,image-family=ubuntu-1604-lts,size=10GB   --network-interface subnet-name=default-ru-central1-a,nat-ip-version=ipv4   --metadata serial-port-enable=1 --metadata-from-file user-data="/home/otus/TapkiPlus_infra/userdata.mime"

testapp_IP = 51.250.8.207
testapp_port = 9292
