LIGA paso a tablas	 	  
	 	

GOLES(id\_gol PK, minuto,id\_partido FK → PARTIDOS, id\_jugador FK → JUGADORES)

EQUIPOS(id\_equipo PK, nombre, ciudad, pabellon)

JUGADOR (id\_jugador PK, nombre,posicion,dorsal,fecha\_nacimiento,id\_equipo FK → EQUIPO)

PARTIDOS(id\_partido PK, jornada, fecha, goles\_local, goles\_visitante, id\_local FK → EQUIPOS, id\_visitante FK → EQUIPOS)
