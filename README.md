# Entrega-Final-Nosql

# realizado con 
*Fuseki
*Sparql

# VIDEO DE COMO USAR FUSEKI
https://youtu.be/jtubggochuk

# MANERA DE REALIZAR LA CONSULTA 
Entra a Fuseki en http://localhost:3030 Como se muestra en el video 
, ya en Fuseki, vaya a "Manage datasets", haga clic en "Add new dataset", marque "Persistent" 
y proporcione el nombre de la base de datos con la cual vamos a realizar las consultas subiendo nuestro archivo ttl

Ahora vaya a Dataset, seleccione el menú desplegable y pruebe "Info and Query". 
Pruebe los siguientes querys como se encuentran en la carpeta de presentacion 

# QUERY

SELECT  (count(distinct ?author) as ?count){

SELECT ?author WHERE {
  
  OPTIONAL { ?documento fabio:JournalArticle ?article}
  
  OPTIONAL { ?documento dc:created ?fecha}
  
  OPTIONAL { ?documento dc:title  ?title}
  
  OPTIONAL { ?documento dc:contributor ?autores}
}
 GROUP BY ?author
 }
LIMIT 25
