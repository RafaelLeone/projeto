# Passo a passo do primeiro teste:  
  
1 - Clone o repositório  
2 - Acesse a pasta clonada (ex.: cd projeto) e depois a pasta do projeto (cd mytodolist)
3 - Rode os seguintes comandos:  
  
docker-compose build  
  
docker-compose up  
  
4 - Acesse localhost em seu navegador para ver a página inicial (com botão de login)  
5 - No terminal digite o seguinte comando para criar um usuário e senha:  
  
./manage.py createsuperuser  
  
6 - Depois de criar o usuário no terminal, volte ao localhost em seu navegador e faça login.  
7 - Adicione suas tarefas :)  


## O que pode dar errado?  
  
1 - Pode haver outro docker rodando. Rode:  
docker-compose down  
Para tirar os containers que subimos agora. Rode:  
docker ps  
Se ainda houver containers pode ser necessário pará-los com:  
docker kill "número-do-container"  

2 - Pode haver portas já sendo utilizadas. Rode:  
netstat -anp|grep "numero-da-porta"  
Esse projeto pode usar as portas 3000, 3001, 80, 8080 e 8000  
Caso haja algum serviço em alguma dessas portas rode:  
kill -9 "numero-do-PID"  
O PID vai ser o número antes da barra na útlima coluna.  
É bom fazer o passo 1 antes de tentar o docker-compose up novamente!


## Créditos ao projeto base:

https://github.com/huogerac/djavue  
https://github.com/evolutio/djavue2 (original)
