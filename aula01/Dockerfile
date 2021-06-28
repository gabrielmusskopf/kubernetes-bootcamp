# CRIAR IMAGEM

# A partir de ubuntu
# É uma boa prática colocar a tag no dockerfile
FROM ubuntu:20.10

# Como a criação de imagem utiliza CACHE, o UPDATE não será realizado
# novamente ao criar a imagem, o que pode levar a instalar um 
# pacote sem ter feito o UPDATE

# RUN apt-get update
# RUN apt-get install curl --yes

# Para resolver, é comum encadear os apt-get
RUN apt-get update && apt-get install curl --yes