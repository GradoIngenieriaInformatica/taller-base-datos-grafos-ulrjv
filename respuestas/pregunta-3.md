MATCH (p:Persona)-[:AMIGO_DE]-(amigo:Persona) WITH p, count(DISTINCT amigo) AS amigos WHERE amigos >= 2 RETURN DISTINCT p.nombre
