## Banco de Dados

  O banco de dados apresenta uma lista de clientes com seus nomes, 
  telefones e cidades onde moram, apresentada abaixo:
   ![alt text]( https://github.com/Shueiz/Plano-de-Melhoria/blob/main/image.png)
   
 ### Análise dos Dados
 
  Dentro dessa lista, caso seja necessário saber, por exemplo, quantas pessoas 
  tem o mesmo nome e qual é esse nome, a sintaxe que foi utilizada para puxar essa informação 
  foi:
  
 > select*from Tbl_Cliente where (nome) in (select nome FROM Tbl_Cliente group by nome having count (distinct id_cliente) > 1) order by nome asc
 
 Resultando nessa tabela:
 
