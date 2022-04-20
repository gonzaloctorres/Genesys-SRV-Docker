**** Docker 1.0

## Sobre o Docker

Caso você não conheça o Docker, leia o manual de como instalar e entender como funciona o Docker.
https://docs.docker.com/desktop/


## Containers
- apache
- php-fpm (com xdebug)
- nodejs


## Configurações

1 - Primeiro instale o docker para ambientes windows pelo link abaixo.
https://docs.docker.com/desktop/windows/install/

2 - Apos isso, temos duas alternativas você baixar esta pasta completa.

	a) Clica no botão verde do lado superior direito e faz o **download ZIP**
	b) baixa a pasta inteira usando o git
		Instala o git:
		https://git-scm.com/download/win
		
		Baixa pelo terminal a pasta completa com o comando:
		
		`git clone https://github.com/gonzaloctorres/Genesys-SRV-Docker.git --depth=100 --recursive`
		
3 - Com os arquivos baixados, acessa o terminal e passa pra etapa de **Instalação**


O arquivo `.env` possui as configurações gerais que serão usadas na instalação do ambiente.

Caso queria alterar a versão do PHP (default=7.4), mudar o valor de `PHP_VERSION`.


## Instalação

Com os arquivos descompactados, basta estar na pasta baixada (do git ou do zip) e executar no terminal conforme descrito abaixo.

Para instalar todos os containers basta fazer `docker-compose up -d --build` nesta pasta raiz.

Instalar:

`docker-compose up -d --build`


## Utilizando o Docker

Use `docker-compose up -d` (nesse ambiente) para iniciar todos os containers quando sua máquina for iniciada.

Para instalar uma nova extensão PHP, você precisa escrever essa instalação `php/Dockerfile` e construir o container novamente. Em https://github.com/mlocati/docker-php-extension-installer, você acha alguns scripts para facilitar essa instalação. 

Caso você precise adicionar alguma coisa no `php.ini`, basta colocar em `php/conf/ambiente.ini` e reinicia os containers. 

