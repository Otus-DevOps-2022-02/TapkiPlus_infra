# TapkiPlus_infra
TapkiPlus Infra repository

ssh -A -i /home/tapkiplus/.ssh/tapkiplus.key -J appuser@51.250.14.154 appuser@10.128.0.17

cat ~/.ssh/config
Host someinternalhost
	HostName 10.128.0.17
	ProxyJump %r@51.250.14.154
	IdentityFile ~/.ssh/imstandby.key
	User appuser
