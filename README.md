Select * FROM 
  (
  SELECT DISTINCT assunto, ano, COUNT(*) AS Quantidade
  FROM atendimentos
  GROUP BY assunto, ano ORDER BY Quantidade DESC
  )
where rownum <= 3;

Código disponível em: https://sqlfiddle.com/#!4/b503f6/31