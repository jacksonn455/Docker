Docker
===============================================

- Verificar a sua versão: <br>
docker version

- Também podemos executar o clássico Hello World: <br>
docker run hello- world

- Imagem do Ubuntu <br>
docker run ubuntu

- Docker irá executar um container com Ubuntu <br>
docker run ubuntu echo "Ola Mundo"

- Terminal do container: <br>
docker run - it ubuntu

- Sair do container <br>
Ctrl + D

- Container a ser iniciado <br>
docker start 2b28c00e8c45
	
- Container a ser parado <br>
docker stop 2b28c00e8c45

- Tempo 0 para parar o container  <br>
docker stop –t 0 2b28c00e8c45

- Interagirmos com o terminal do container criado <br>
docker start - a - i 2b28c00e8c45

- Listar os containers, menos os parados <br>
docker ps

- Listar apenas id <br>
docker ps - q

- Listar os containers, até os parados <br>
docker ps - a

- Remover os containers <br>
docker rm 2b28c00e8c45

- Remove todos containers inativos <br>
docker container prune

- Mostra as imagens <br>
docker imagens

- Remover imagens <br>
docker rmi hello- world
- Forçando remoção de imagem <br>
docker rmi hello- world - f

- Container que segurará um site estático ( - P mapeia uma porta aleatória ) <br>
docker run - d –P dockersamples/static- site
- Depois ver a porta usada <br>
http://localhost:49154/

- Mapeia uma porta especifica ( ) <br>
docker run - d - p 12345:80 dockersamples/static- site

- Depois ver a porta usada <br>
http://localhost:12345/

- Nome do container para ficar mais fácil de parar ele <br>
docker run - d - P - - name meu- site dockersamples/static- site

- Parar container pelo nome <br>
docker stop meu- site

- Ver a porta que esta sendo usada <br>
docker port 2b28c00e8c45

- Variavel de ambiente (- e) <br>
docker run - d - P - e AUTHOR="Jackson Magnabosco" dockersamples/static- site

- utilizando a flag - v para criar um volume <br>
docker run - v "/var/www" ubuntu

- Pasta salva no desktop  <br>
docker run - it - v "C:\Users\Avell\Desktop:/var/www" Ubuntu

- Inspecionar o container <br>
docker inspect

- docker pull NOME_USUARIO/NOME_IMAGEM
- docker pull douglasq/alura- books:cap05

- Log <br>
docker logs - f - t - - tail 100 anymarket- cache  // log em tempo real

- Examinar container  <br>
docker exec - it <container- id> /bin/sh

-- 

- Docker-Compose

- Listar os containers <br>
docker- compose ps - - service

- Log <br>
docker- compose logs - f - t - - tail 100  indexador  // log em tempo real
docker- compose logs

- Derruba o container <br>
docker- compose down

- Constroi o container <br>
docker- compose build

- Sobe container <br>
docker- compose up - d
