FROM node:14-alpine
#se tiver uma pasta entro nessa caso não tenho eu crio e entro nela 
WORKDIR /backend-app
# a porta 3001 padrão do alpine(conatiner)
EXPOSE 3001
#copiar tudo que tá na pasta back-end para a raiz que estou 
COPY . .
#COPIA E DESCOMPACTA
ADD ./node_modules.tar.gz .
#após toda construção rodamos o comando renicialização
CMD [ "npm", "start" ]