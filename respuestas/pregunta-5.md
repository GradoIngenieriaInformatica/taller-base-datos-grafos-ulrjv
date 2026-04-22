MATCH (p:Persona)-[:AMIGO_DE]-(amigo:Persona)-[:PARTICIPA_EN]->(pr:Proyecto) WITH p, amigo, count(DISTINCT pr) AS proyectos WHERE proyectos > 1 RETURN DISTINCT p.nombre
