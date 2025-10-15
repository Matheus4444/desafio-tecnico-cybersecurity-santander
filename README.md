# Desafio Técnico Cyber Security Santander
Este repositório contém o desdobramento do desafio técnico proposto pelo curso de Cyber Security do Santander, os passos tomados para solucionar os desafios propostos e como foram utilizadas as ferramentas disponíveis.

O desafio consiste em fazer o setup de duas máquinas virtuais, uma contendo a distro Kali Linux, outra contendo o Metasploitable 2, e utilizar a ferramenta Medusa para realizar uma série de ataques.
O primeiro ataque consiste em um brute force em FTP utilizando duas wordlists criadas pelo atacante e um comando do Medusa que recebe o IP da máquina alvo e as wordlists, para tentar combinações possíveis de usuário e senha.
O segundo ataque consiste em realizar um brute force no site propositalmente vulnerável DVWA, também hosteado na máquina previamente alvejada, utilizando um comando do Medusa que recebe o IP alvo, a página alvo, uma wordlist de usuários, uma de senhas e como o formulário http é estruturado, para crackear a combinação correta de usuário e senha.
O terceiro e último ataque consiste em realizar um password spraying em SMB utilizando enumeração de usuários. Para isso, foi utilizada a ferramenta enum4linux, que extraiu uma série de informações sobre a máquina alvo, incluindo a lista de usuários da mesma. Foi utilizada essa lista, em conjunto com uma wordlist de senhas comumente utilizadas, criada com base em relatórios de vazamentos ao redor do globo, em um comando do Medusa que recebe as duas listas, o IP alvo e a quantidades de hosts rodando em paralelo.

Todos os passos realizados estão documentados por print na pasta images, e todos os comandos utilizados foram armazenados no arquivo comandos-utilizados.txt.
