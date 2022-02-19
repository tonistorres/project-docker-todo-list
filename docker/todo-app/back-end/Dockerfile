# node:14-alpine - Alpane é uma das distribuições línux nesse 
# caso em específico muito básica, pequena suficiente para caber
# em um pendrive, estamos pedindo para construir um 
# ambiente alpani com o node dentro intalado para rodar nosso 
# arquivos contido dentro da pasta back-end
# https://www.youtube.com/watch?v=FX8cev-4qNo
# https://github.com/nodejs/docker-node

FROM node:14-alpine
# É muito comum definirmos um pasta de trabalho dentro do container
# que irá hospedar nossos arquivos que serão servidos pele alpine node.
# Neste caso específico estamos pedindo que o comando WORKDIR crie um 
# uma pasta /backend-app dentro do linux alpine onde serão servido nossos 
# arquivos que serão enviados por meio do comando COPY logo abaixo explicitado
WORKDIR /backend-app

#A instrução EXPOSE na verdade não publica a porta.
# Funciona como um tipo de documentação entre a pessoa 
# que constrói a imagem e a pessoa que executa o container,
EXPOSE 3001
# Neste Dockerfile específico o comando COPY esta usando . (PONTO) . (PONTO) para
# Especificar a pasta origem (vale apenas deixar nítido que essa pasta origem se refere
# a origem onde se encontra o arquivo docker file projeto ou arquivo que irá subir para o alpine)
# e pasta de destino (onde está setado WORKDIR que em nosso exemplo aqui explicitado nos nos encontramos
# dentro de /backend-app), ou seja, iremos compiar todos os arquivos locais da maquina hospediera 
# que se encontra dentro de /docker/docker-commands/todo-app/back-end para dentro do container na pasta 
# /back-end onde o meu site, ou arquivos, serão servidos
COPY . .
#COPIA E DESCOMPACTA
ADD ./node_modules.tar.gz .
#após toda construção rodamos o comando renicialização
CMD [ "npm", "start" ]