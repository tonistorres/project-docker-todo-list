# O Dockerfile deve rodar a imagem mjgargani/puppeteer:trybe1.0 para que os testes funcionem;
FROM mjgargani/puppeteer:trybe1.0
#se tiver uma pasta entro nessa caso não tenho eu crio e entro nela 
WORKDIR /tests-app
#Deve adicionar o arquivo node_modules.tar.gz a imagem
ADD node_modules.tar.gz .
#Deve copiar todos os arquivos da pasta tests para a imagem;
COPY . .
#Ao iniciar a imagem deve rodar o comando npm test;
CMD [ "npm", "test" ]