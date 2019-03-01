# Consulta SQL

#### PDF - Protocolo Documentos e fluxos


SELECT DISTINCT a.numeroorigem, a.registro, c.nome,  f.nome as nome_funcionario FROM pdfdocumento a inner Join
pdfdoctipomodelo b on a.tipo = b.documentotipo inner Join 
pdftipodocumento c on  b.nome = c.Nome inner Join 
pdfusuariolocal d on a.usuario = d.usuario inner Join
gfpfuncionario f on d.lotacao = f.matricula
where a.tipo = 12 and a.registro BETWEEN '01-01-2018' and '31-12-2018'
order by a.numeroorigem asc;
