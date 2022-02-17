# Docker Apache2+PHP5.6

## Conteúdo
Neste projeto está incluido:
	PHP: 5.6
	Apache: 2.4

### Build da imagem

Comando para criar a imagem

```
docker build -t aplicação .
```

### Up do container

Comando para rodar o container

```
docker run -d -p 8080:80 --name aplicação -v "$PWD":/var/www/html php:5.6-apache
```

### Acessar o container no modo interativo

Comando para acessar o container

```
docker exec -it aplicação bash
```

### Outros comandos necessários do docker

```
attach     : Anexar a um recipiente em execução
build      : Cria uma imagem a partir de um Dockerfile
commit     : Crie uma nova imagem a partir das alterações de um recipiente
cp         : Copie arquivos / pastas entre um contêiner e o sistema de arquivos local
create     : Criar um novo recipiente
diff       : Inspecionar alterações no sistema de arquivos de um contêiner
events     : Obtenha eventos em tempo real do servidor
exec       : Execute um comando em um recipiente em execução
export     : Exportar o sistema de arquivos de um recipiente como um arquivo tar
history    : Mostra a história de uma imagem
images     : Listar imagens
import     : Importar o conteúdo de um tarball para criar uma imagem do sistema de arquivos
info       : Exibir informações em todo o sistema
inspect    : Retornar informações de baixo nível em um recipiente, imagem ou tarefa
kill       : Mata um ou mais recipientes em execução
load       : Carrega uma imagem de um arquivo tar ou STDIN
login      : Faz logon em um registro Docker.
logout     : Sai de um registro do Docker.
logs       : Busca os logs de um recipiente
network    : Gerencia redes Docker
node       : Gerencia os nós Docker Swarm
pause      : Pausa todos os processos dentro de um ou mais recipientes
port       : Lista mapeamentos de porta ou um mapeamento específico para o contêiner
ps         : Lista de contêineres
pull       : Puxa uma imagem ou um repositório de um registro
push       : Empurra uma imagem ou um repositório para um registro
rename     : Muda o nome de um recipiente
restart    : Reinicia um recipiente
rm         : Remove um ou mais recipientes
rmi        : Remove uma ou mais imagens
run        : Executa um comando em um novo recipiente
save       : Salva uma ou mais imagens em um arquivo tar (transmitido para STDOUT por padrão)
search     : Procura o Docker Hub para imagens
service    : Gerencia serviços Docker
start      : Começa um ou mais containner parado
stats      : Exibi uma transmissão ao vivo de estatísticas de uso de recursos de contêineres
stop       : Para um ou mais recipientes em execução
swarm      : Gerencia Docker Swarm
tag        : Marca uma imagem em um repositório
top        : Exibe os processos em execução de um recipiente
unpause    : Desativa todos os processos dentro de um ou mais recipientes
update     : Atualiza a configuração de um ou mais recipientes
version    : Mostra as informações da versão do Docker
volume     : Gerencia volumes do Docker
wait       : Bloqueia até um recipiente parar e, em seguida, imprima seu código de saída
```