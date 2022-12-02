# Banco de Dados

  O banco de dados apresenta uma lista de clientes com seus nomes, 
  telefones e cidades onde moram, apresentada abaixo:
  
   ![alt text]( https://github.com/Shueiz/Plano-de-Melhoria/blob/main/Imagens/imagem_2022-12-02_141549149.png)
   
 ## Análise dos Dados
 
 ### Região Mais Acessada
 
  Dentro dessa lista, caso seja necessário saber o DDD de um cliente, o código usado para puxar essa informação foi: 
  
 > select*from TabelaClientes where DDD = '(63)'; 
 
 Resultando nessa tabela:
 
 ![alt text]( https://github.com/Shueiz/Plano-de-Melhoria/blob/main/Imagens/imagem_2022-12-02_141946854.png)
 
 Com essa tabela é possível perceber que dos 32 usuários cadastrados, 
 20 deles se encontram no estado do Tocatins, mostrando que o público 
 alvo é voltado para a Região Norte, mais especificamente no Estado do Tocatins
 
 Enquanto aos outros 12 usuários, mostrado nessa tabela abaixo: 
 
 ![alt text]( https://github.com/Shueiz/Plano-de-Melhoria/blob/main/Imagens/imagem_2022-12-02_142403854.png)
 
 Esses 12 usuários se localizam na Região Centro-Oeste, mais especificamente no Estado de Goiás 

 
 ### Cidade com mais Usuários
 
 Caso seja necessário saber qual a cidade com mais usuários, o 
 código utilizado para buscar essa informação é 
  
  > SELECT 
   cidade, 
   count(*) AS total_por_cidade 
FROM TabelaClientes
WHERE cidade IS NOT NULL
GROUP BY cidade
ORDER BY count(*) desc
  
  Resultando nessa tabela: 
  
  ![alt text](  https://github.com/Shueiz/Plano-de-Melhoria/blob/main/Imagens/imagem_2022-11-25_185343284.png)
  
 
