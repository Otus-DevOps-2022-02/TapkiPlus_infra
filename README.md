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

