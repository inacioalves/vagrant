# Máquina Virtual Vagrant IFCE

## 

### Pré-requisitos

Para continuar, você deve instalar os seguintes softwares na sua máquina:

1. Instale o ***Vagrant***. Ele é uma ferramenta para gerenciar máquinas virtuais
de *hypervisors* como VirtualBox, VMWare etc.: http://www.vagrantup.com/downloads
   * Em sistemas baseados no Debian/Ubuntu, use
   ```bash
   $ sudo apt-get install vagrant
   ```

2. Instale o ***VirtualBox***. Este será o *hypervisor* usado. https://www.virtualbox.org/wiki/Downloads

3. Instale o ***Git*** para sistema de controle de versão.
   * Em sistemas baseados no Debian/Ubuntu, use
   ```bash
   $ sudo apt-get install git
   ```

###

* Clone o repositório a partir do Github:
   ```bash
   $ git clone https://github.com/inacioalves/vagrant seu-nome
   ```

* Entre no diretório criado
   ```bash
   $ cd seu-nome
   ```

* Obtenha uma cópia do **box** com seu professor e adicione o mesmo para que
o Vagrant possa gerenciá-lo
   ```bash
   $ vagrant box add ubuntu ubuntu.box
   ```

* Execute o comando *vagrant up*, este comando lerá o arquivo Vagrantfile do
diretório atual e iniciará a Máquina Virtual seguindo as configurações.
   ```bash
   $ vagrant up
   ```

Para desligar sua Máquina Virtual, você pode usar uma das opções abaixo:
* **vagrant suspend:** Desligará sua máquina salvando o estado atual, assim
você poderá

### Referências
* https://blog.engineyard.com/2014/building-a-vagrant-box
* https://gordonlesti.com/create-debian-8-jessie-vagrant-box/
* https://scotch.io/tutorials/how-to-create-a-vagrant-base-box-from-an-existing-one
