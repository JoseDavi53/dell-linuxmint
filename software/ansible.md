#Autor: Robson Vaamonde<br>
#Procedimentos em TI: http://procedimentosemti.com.br<br>
#Bora para Prática: http://boraparapratica.com.br<br>
#Robson Vaamonde: http://vaamonde.com.br<br>
#Facebook Procedimentos em TI: https://www.facebook.com/ProcedimentosEmTi<br>
#Facebook Bora para Prática: https://www.facebook.com/BoraParaPratica<br>
#Instagram Procedimentos em TI: https://www.instagram.com/procedimentoem<br>
#YouTUBE Bora Para Prática: https://www.youtube.com/boraparapratica<br>
#Data de criação: 31/05/2022<br>
#Data de atualização: 31/05/2022<br>
#Versão: 0.01<br>
#Testado e homologado no Linux Mint 20.1 Ulyssa, 20.2 Uma e 20.3 Una x64

#Instalação do Docker no Linux Mint 20.1 Ulyssa, 20.2 Uma e 20.3 Una x64

#01_ Atualização do Sistema Operacional Linux Mint<br>

	sudo apt update
	sudo apt upgrade
	sudo apt full-upgrade
	sudo apt dist-upgrade
	sudo apt autoremove
	sudo apt autoclean

#02_ Instalando Ansible no Linux Mint<br>

	sudo apt install ansible

#03_ Verificando a Versão do Ansible<br>

	ansible --version

#04_ Criando o Arquivo de Inventário dos Hosts do Ansible

	sudo vim /etc/ansible/hosts
		[servers]
		ptispo01ws01 ansible_host=172.16.1.20

		[all:vars]
		ansible_python_interpreter=/usr/bin/python3
	ansible-inventory --list -y

#5_ Testando a conexão do Ansible com o Host Remoto<br>

	ansible all -m ping -u vaamonde

#06_ Executando um comando no Host Remoto<br>

	ansible all -a "df -h" -u vaamonde
