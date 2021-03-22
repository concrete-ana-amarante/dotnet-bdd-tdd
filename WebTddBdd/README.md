### Gerar build do donet ###
donet build

### Gerar o build do docker
docker build -t concreteanaamarante/validador-cpf-dotnet -f Dockerfile .

### Rodar imagem docker e gravar localmente ###
docker run -d -p 5001:80 --name validador-cpf-dotnet concreteanaamarante/validador-cpf-dotnet

### Gerar tag ###
docker tag concreteanaamarante/validador-cpf-dotnet 

### Push da imagem para o dockerhub ###
docker push concreteanaamarante/validador-cpf-dotnet